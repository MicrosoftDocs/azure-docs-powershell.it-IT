---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ad57558eeaa9480e6574b74d052131700feaefae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688382"
---
# <span data-ttu-id="4047a-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4047a-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4047a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4047a-102">SYNOPSIS</span></span>
<span data-ttu-id="4047a-103">Salva una configurazione di peering ExpressRoute modificata.</span><span class="sxs-lookup"><span data-stu-id="4047a-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4047a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4047a-104">SYNTAX</span></span>

### <span data-ttu-id="4047a-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4047a-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4047a-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="4047a-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4047a-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="4047a-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4047a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4047a-108">DESCRIPTION</span></span>
<span data-ttu-id="4047a-109">I cmdlet **set-AzureRmExpressRouteCircuitPeeringConfig** salvano una configurazione peer modificata di ExpressRoute in Azure.</span><span class="sxs-lookup"><span data-stu-id="4047a-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="4047a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4047a-110">EXAMPLES</span></span>

### <span data-ttu-id="4047a-111">Esempio 1: modificare una configurazione peer esistente</span><span class="sxs-lookup"><span data-stu-id="4047a-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="4047a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4047a-112">PARAMETERS</span></span>

### <span data-ttu-id="4047a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4047a-113">-DefaultProfile</span></span>
<span data-ttu-id="4047a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4047a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4047a-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4047a-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4047a-116">L'oggetto Circuit ExpressRoute che contiene la configurazione peer da modificare.</span><span class="sxs-lookup"><span data-stu-id="4047a-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4047a-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="4047a-117">-LegacyMode</span></span>
<span data-ttu-id="4047a-118">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="4047a-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="4047a-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="4047a-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="4047a-120">Per un PeeringType di MicrosoftPeering, è necessario specificare un elenco di tutti i prefissi che si prevede di pubblicizzare durante la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="4047a-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="4047a-121">Vengono accettati solo i prefissi degli indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="4047a-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="4047a-122">Se si prevede di inviare un set di prefissi, è possibile inviare un elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="4047a-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="4047a-123">Questi prefissi devono essere registrati in un nome del registro di sistema di routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="4047a-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="4047a-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="4047a-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="4047a-125">Per i prefissi pubblicitari non registrati nel numero di peering, è possibile specificare il numero di come registrato.</span><span class="sxs-lookup"><span data-stu-id="4047a-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="4047a-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="4047a-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="4047a-127">Il nome del registro di sistema di routing (RIR/IRR) a cui sono registrati il numero e i prefissi come.</span><span class="sxs-lookup"><span data-stu-id="4047a-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="4047a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4047a-128">-Name</span></span>
<span data-ttu-id="4047a-129">Nome della configurazione peer da modificare.</span><span class="sxs-lookup"><span data-stu-id="4047a-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4047a-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4047a-130">-PeerAddressType</span></span>
<span data-ttu-id="4047a-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4047a-131">PeerAddressType</span></span>

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

### <span data-ttu-id="4047a-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="4047a-132">-PeerASN</span></span>
<span data-ttu-id="4047a-133">Numero come del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4047a-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="4047a-134">Deve essere un ASN pubblico quando PeeringType è AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="4047a-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="4047a-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4047a-135">-PeeringType</span></span>
<span data-ttu-id="4047a-136">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4047a-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4047a-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4047a-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="4047a-138">Questo è l'intervallo di indirizzi IP per il percorso di routing principale di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="4047a-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="4047a-139">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="4047a-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4047a-140">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="4047a-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4047a-141">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="4047a-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4047a-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4047a-142">-RouteFilter</span></span>
<span data-ttu-id="4047a-143">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="4047a-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4047a-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="4047a-144">-RouteFilterId</span></span>
<span data-ttu-id="4047a-145">Questo è l'ID risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="4047a-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4047a-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4047a-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="4047a-147">Questo è l'intervallo di indirizzi IP per il percorso di routing secondario di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="4047a-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="4047a-148">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="4047a-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4047a-149">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="4047a-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4047a-150">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="4047a-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4047a-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4047a-151">-SharedKey</span></span>
<span data-ttu-id="4047a-152">Si tratta di un hash MD5 facoltativo usato come chiave già condivisa per la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="4047a-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="4047a-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="4047a-153">-VlanId</span></span>
<span data-ttu-id="4047a-154">Questo è il numero ID della VLAN assegnata per questo peering.</span><span class="sxs-lookup"><span data-stu-id="4047a-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="4047a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4047a-155">CommonParameters</span></span>
<span data-ttu-id="4047a-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4047a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4047a-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4047a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4047a-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4047a-158">INPUTS</span></span>

### <span data-ttu-id="4047a-159">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4047a-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="4047a-160">Parametri: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4047a-160">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="4047a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4047a-161">System.String</span></span>

### <span data-ttu-id="4047a-162">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4047a-162">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="4047a-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4047a-163">System.Boolean</span></span>

## <span data-ttu-id="4047a-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4047a-164">OUTPUTS</span></span>

### <span data-ttu-id="4047a-165">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4047a-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4047a-166">Note</span><span class="sxs-lookup"><span data-stu-id="4047a-166">NOTES</span></span>

## <span data-ttu-id="4047a-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4047a-167">RELATED LINKS</span></span>

[<span data-ttu-id="4047a-168">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4047a-168">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4047a-169">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4047a-169">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4047a-170">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4047a-170">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4047a-171">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4047a-171">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)