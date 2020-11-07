---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 3a97562c775c901e8226d1dc5a0b9d090f8f70cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862802"
---
# <span data-ttu-id="f8856-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8856-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f8856-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8856-102">SYNOPSIS</span></span>
<span data-ttu-id="f8856-103">Salva una configurazione di peering ExpressRoute modificata.</span><span class="sxs-lookup"><span data-stu-id="f8856-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="f8856-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8856-104">SYNTAX</span></span>

### <span data-ttu-id="f8856-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8856-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8856-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="f8856-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8856-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="f8856-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8856-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8856-108">DESCRIPTION</span></span>
<span data-ttu-id="f8856-109">I cmdlet **set-AzExpressRouteCircuitPeeringConfig** salvano una configurazione peer modificata di ExpressRoute in Azure.</span><span class="sxs-lookup"><span data-stu-id="f8856-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="f8856-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8856-110">EXAMPLES</span></span>

### <span data-ttu-id="f8856-111">Esempio 1: modificare una configurazione peer esistente</span><span class="sxs-lookup"><span data-stu-id="f8856-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="f8856-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8856-112">PARAMETERS</span></span>

### <span data-ttu-id="f8856-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8856-113">-DefaultProfile</span></span>
<span data-ttu-id="f8856-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8856-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8856-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f8856-116">L'oggetto Circuit ExpressRoute che contiene la configurazione peer da modificare.</span><span class="sxs-lookup"><span data-stu-id="f8856-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="f8856-117">-LegacyMode</span></span>
<span data-ttu-id="f8856-118">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="f8856-118">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="f8856-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="f8856-120">Per un PeeringType di MicrosoftPeering, è necessario specificare un elenco di tutti i prefissi che si prevede di pubblicizzare durante la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="f8856-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="f8856-121">Vengono accettati solo i prefissi degli indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="f8856-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="f8856-122">Se si prevede di inviare un set di prefissi, è possibile inviare un elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="f8856-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="f8856-123">Questi prefissi devono essere registrati in un nome del registro di sistema di routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="f8856-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="f8856-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="f8856-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="f8856-125">Per i prefissi pubblicitari non registrati nel numero di peering, è possibile specificare il numero di come registrato.</span><span class="sxs-lookup"><span data-stu-id="f8856-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="f8856-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="f8856-127">Il nome del registro di sistema di routing (RIR/IRR) a cui sono registrati il numero e i prefissi come.</span><span class="sxs-lookup"><span data-stu-id="f8856-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8856-128">-Name</span></span>
<span data-ttu-id="f8856-129">Nome della configurazione peer da modificare.</span><span class="sxs-lookup"><span data-stu-id="f8856-129">The name of the peering configuration to be modified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f8856-130">-PeerAddressType</span></span>
<span data-ttu-id="f8856-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f8856-131">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="f8856-132">-PeerASN</span></span>
<span data-ttu-id="f8856-133">Numero come del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8856-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="f8856-134">Deve essere un ASN pubblico quando PeeringType è AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="f8856-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f8856-135">-PeeringType</span></span>
<span data-ttu-id="f8856-136">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f8856-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8856-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="f8856-138">Questo è l'intervallo di indirizzi IP per il percorso di routing principale di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="f8856-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="f8856-139">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="f8856-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f8856-140">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="f8856-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f8856-141">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="f8856-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f8856-142">-RouteFilter</span></span>
<span data-ttu-id="f8856-143">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="f8856-143">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="f8856-144">-RouteFilterId</span></span>
<span data-ttu-id="f8856-145">Questo è l'ID risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="f8856-145">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8856-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="f8856-147">Questo è l'intervallo di indirizzi IP per il percorso di routing secondario di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="f8856-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="f8856-148">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="f8856-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f8856-149">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="f8856-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f8856-150">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="f8856-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f8856-151">-SharedKey</span></span>
<span data-ttu-id="f8856-152">Si tratta di un hash MD5 facoltativo usato come chiave già condivisa per la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="f8856-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="f8856-153">-VlanId</span></span>
<span data-ttu-id="f8856-154">Questo è il numero ID della VLAN assegnata per questo peering.</span><span class="sxs-lookup"><span data-stu-id="f8856-154">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8856-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8856-155">CommonParameters</span></span>
<span data-ttu-id="f8856-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8856-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8856-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8856-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8856-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8856-158">INPUTS</span></span>

### <span data-ttu-id="f8856-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8856-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="f8856-160">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f8856-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="f8856-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8856-161">OUTPUTS</span></span>

### <span data-ttu-id="f8856-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8856-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f8856-163">Note</span><span class="sxs-lookup"><span data-stu-id="f8856-163">NOTES</span></span>

## <span data-ttu-id="f8856-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8856-164">RELATED LINKS</span></span>

[<span data-ttu-id="f8856-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8856-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8856-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8856-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f8856-167">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8856-167">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8856-168">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8856-168">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
