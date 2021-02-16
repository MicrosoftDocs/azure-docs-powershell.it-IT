---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203198"
---
# <span data-ttu-id="8c797-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8c797-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="8c797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c797-102">SYNOPSIS</span></span>
<span data-ttu-id="8c797-103">Aggiunge una configurazione di peering a una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8c797-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8c797-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c797-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c797-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c797-105">DESCRIPTION</span></span>
<span data-ttu-id="8c797-106">Il cmdlet **Add-AzExpressRouteCrossConnectionEndoing** aggiunge una configurazione di peering a una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8c797-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="8c797-107">Si noti che, dopo aver eseguito **Add-AzExpressRouteCrossConnection Sempreing,** è necessario chiamare il cmdlet Set-AzExpressRouteCrossConnection per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="8c797-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="8c797-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c797-108">EXAMPLES</span></span>

### <span data-ttu-id="8c797-109">Esempio 1: Aggiungere un peer a una connessione incrociata ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="8c797-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="8c797-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c797-110">PARAMETERS</span></span>

### <span data-ttu-id="8c797-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c797-111">-DefaultProfile</span></span>
<span data-ttu-id="8c797-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c797-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c797-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8c797-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8c797-114">La connessione incrociata ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="8c797-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="8c797-115">Oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCrossConnection.**</span><span class="sxs-lookup"><span data-stu-id="8c797-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="8c797-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8c797-116">-Force</span></span>
<span data-ttu-id="8c797-117">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="8c797-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8c797-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="8c797-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="8c797-119">Per un PeeringType di MicrosoftIing, è necessario fornire un elenco di tutti i prefissi che si prevede di annunciare tramite la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="8c797-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="8c797-120">Vengono accettati solo i prefissi di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="8c797-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="8c797-121">È possibile inviare un elenco separato da virgole se si prevede di inviare un set di prefissi.</span><span class="sxs-lookup"><span data-stu-id="8c797-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="8c797-122">Questi prefissi devono essere registrati in un nome registro di routing (RIR/TIR.IRR).</span><span class="sxs-lookup"><span data-stu-id="8c797-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="8c797-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="8c797-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="8c797-124">Se si stanno annunciando prefissi non registrati nel numero AS di peering, è possibile specificare il numero AS con cui vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="8c797-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="8c797-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="8c797-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="8c797-126">Nome del Registro di sistema di routing (RIR/TIR.IRR) in cui vengono registrati il numero AS e i prefissi.</span><span class="sxs-lookup"><span data-stu-id="8c797-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="8c797-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8c797-127">-Name</span></span>
<span data-ttu-id="8c797-128">Nome della relazione di peering da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="8c797-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="8c797-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8c797-129">-PeerAddressType</span></span>
<span data-ttu-id="8c797-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8c797-130">PeerAddressType</span></span>

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

### <span data-ttu-id="8c797-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="8c797-131">-PeerASN</span></span>
<span data-ttu-id="8c797-132">Il numero AS della connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8c797-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="8c797-133">Deve essere un ASN pubblico quando PeeringType è AzurePublicApplicationing.</span><span class="sxs-lookup"><span data-stu-id="8c797-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="8c797-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8c797-134">-PeeringType</span></span>
<span data-ttu-id="8c797-135">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8c797-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8c797-136">-PrimaryAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8c797-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="8c797-137">Intervallo di indirizzi IP per il percorso di routing principale di questa relazione di peering.</span><span class="sxs-lookup"><span data-stu-id="8c797-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="8c797-138">Deve essere una subnet CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="8c797-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8c797-139">Il primo indirizzo con numero dispari in questa subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="8c797-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8c797-140">Azure configurerà il successivo indirizzo pari all'interfaccia del router di Azure.</span><span class="sxs-lookup"><span data-stu-id="8c797-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8c797-141">-SecondaryAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8c797-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="8c797-142">Intervallo di indirizzi IP per il percorso di routing secondario di questa relazione di peering.</span><span class="sxs-lookup"><span data-stu-id="8c797-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="8c797-143">Deve essere una subnet CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="8c797-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8c797-144">Il primo indirizzo con numero dispari in questa subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="8c797-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8c797-145">Azure configurerà il successivo indirizzo pari all'interfaccia del router di Azure.</span><span class="sxs-lookup"><span data-stu-id="8c797-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8c797-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8c797-146">-SharedKey</span></span>
<span data-ttu-id="8c797-147">Questo è un hash MD5 facoltativo usato come chiave pre-condivisa per la configurazione del peering.</span><span class="sxs-lookup"><span data-stu-id="8c797-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="8c797-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="8c797-148">-VlanId</span></span>
<span data-ttu-id="8c797-149">Id della VLAN assegnata al peering.</span><span class="sxs-lookup"><span data-stu-id="8c797-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="8c797-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c797-150">-Confirm</span></span>
<span data-ttu-id="8c797-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c797-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c797-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c797-152">-WhatIf</span></span>
<span data-ttu-id="8c797-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c797-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c797-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c797-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c797-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c797-155">CommonParameters</span></span>
<span data-ttu-id="8c797-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c797-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c797-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c797-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c797-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c797-158">INPUTS</span></span>

### <span data-ttu-id="8c797-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8c797-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="8c797-160">Il parametro 'ExpressRouteCrossConnection' accetta il valore di tipo 'PSExpressRouteCrossConnection' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8c797-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="8c797-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c797-161">OUTPUTS</span></span>

### <span data-ttu-id="8c797-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8c797-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="8c797-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c797-163">NOTES</span></span>

## <span data-ttu-id="8c797-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c797-164">RELATED LINKS</span></span>

[<span data-ttu-id="8c797-165">Get-AzExpressRouteCrossConnectionEndoing</span><span class="sxs-lookup"><span data-stu-id="8c797-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="8c797-166">Remove-AzExpressRouteCrossConnectionEndoing</span><span class="sxs-lookup"><span data-stu-id="8c797-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="8c797-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8c797-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="8c797-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8c797-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
