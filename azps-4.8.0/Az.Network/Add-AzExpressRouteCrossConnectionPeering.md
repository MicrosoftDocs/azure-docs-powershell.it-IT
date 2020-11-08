---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192857"
---
# <span data-ttu-id="6c9de-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6c9de-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="6c9de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c9de-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9de-103">Aggiunge una configurazione peering a una connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6c9de-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="6c9de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c9de-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c9de-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9de-106">Il cmdlet **Add-AzExpressRouteCrossConnectionPeering** aggiunge una configurazione peer a una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6c9de-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="6c9de-107">Tieni presente che, dopo aver eseguito **Add-AzExpressRouteCrossConnectionPeering** , devi chiamare il cmdlet Set-AzExpressRouteCrossConnection per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="6c9de-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="6c9de-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c9de-108">EXAMPLES</span></span>

### <span data-ttu-id="6c9de-109">Esempio 1: aggiungere un peer a una connessione incrociata di ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="6c9de-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="6c9de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c9de-110">PARAMETERS</span></span>

### <span data-ttu-id="6c9de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9de-111">-DefaultProfile</span></span>
<span data-ttu-id="6c9de-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9de-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6c9de-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="6c9de-114">La connessione trasversale ExpressRoute viene modificata.</span><span class="sxs-lookup"><span data-stu-id="6c9de-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="6c9de-115">Questo è un oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCrossConnection** .</span><span class="sxs-lookup"><span data-stu-id="6c9de-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9de-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6c9de-116">-Force</span></span>
<span data-ttu-id="6c9de-117">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="6c9de-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9de-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9de-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="6c9de-119">Per un PeeringType di MicrosoftPeering, è necessario specificare un elenco di tutti i prefissi che si prevede di pubblicizzare durante la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="6c9de-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="6c9de-120">Vengono accettati solo i prefissi degli indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="6c9de-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="6c9de-121">Se si prevede di inviare un set di prefissi, è possibile inviare un elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="6c9de-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="6c9de-122">Questi prefissi devono essere registrati in un nome del registro di sistema di routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="6c9de-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="6c9de-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="6c9de-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="6c9de-124">Per i prefissi pubblicitari non registrati nel numero di peering, è possibile specificare il numero di come registrato.</span><span class="sxs-lookup"><span data-stu-id="6c9de-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="6c9de-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="6c9de-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="6c9de-126">Il nome del registro di sistema di routing (RIR/IRR) a cui sono registrati il numero e i prefissi come.</span><span class="sxs-lookup"><span data-stu-id="6c9de-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="6c9de-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c9de-127">-Name</span></span>
<span data-ttu-id="6c9de-128">Nome della relazione peering da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6c9de-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="6c9de-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="6c9de-129">-PeerAddressType</span></span>
<span data-ttu-id="6c9de-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="6c9de-130">PeerAddressType</span></span>

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

### <span data-ttu-id="6c9de-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="6c9de-131">-PeerASN</span></span>
<span data-ttu-id="6c9de-132">Numero come della connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6c9de-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="6c9de-133">Deve essere un ASN pubblico quando PeeringType è AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="6c9de-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="6c9de-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6c9de-134">-PeeringType</span></span>
<span data-ttu-id="6c9de-135">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6c9de-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="6c9de-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9de-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="6c9de-137">Questo è l'intervallo di indirizzi IP per il percorso di routing principale di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="6c9de-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="6c9de-138">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="6c9de-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="6c9de-139">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="6c9de-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="6c9de-140">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="6c9de-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="6c9de-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6c9de-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="6c9de-142">Questo è l'intervallo di indirizzi IP per il percorso di routing secondario di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="6c9de-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="6c9de-143">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="6c9de-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="6c9de-144">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="6c9de-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="6c9de-145">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="6c9de-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="6c9de-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6c9de-146">-SharedKey</span></span>
<span data-ttu-id="6c9de-147">Si tratta di un hash MD5 facoltativo usato come chiave già condivisa per la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="6c9de-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="6c9de-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="6c9de-148">-VlanId</span></span>
<span data-ttu-id="6c9de-149">Questo è il numero ID della VLAN assegnata per questo peering.</span><span class="sxs-lookup"><span data-stu-id="6c9de-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="6c9de-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c9de-150">-Confirm</span></span>
<span data-ttu-id="6c9de-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9de-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9de-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9de-152">-WhatIf</span></span>
<span data-ttu-id="6c9de-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c9de-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c9de-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c9de-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9de-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9de-155">CommonParameters</span></span>
<span data-ttu-id="6c9de-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9de-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9de-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9de-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9de-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c9de-158">INPUTS</span></span>

### <span data-ttu-id="6c9de-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6c9de-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="6c9de-160">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6c9de-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="6c9de-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c9de-161">OUTPUTS</span></span>

### <span data-ttu-id="6c9de-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6c9de-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="6c9de-163">Note</span><span class="sxs-lookup"><span data-stu-id="6c9de-163">NOTES</span></span>

## <span data-ttu-id="6c9de-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c9de-164">RELATED LINKS</span></span>

[<span data-ttu-id="6c9de-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6c9de-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="6c9de-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6c9de-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="6c9de-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6c9de-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="6c9de-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6c9de-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)