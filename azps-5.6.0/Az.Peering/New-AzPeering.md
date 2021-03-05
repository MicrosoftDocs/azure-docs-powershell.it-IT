---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: d8ef4378ed0032012a64d015855ca0287d608a6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989447"
---
# <span data-ttu-id="a9970-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a9970-101">New-AzPeering</span></span>

## <span data-ttu-id="a9970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9970-102">SYNOPSIS</span></span>
<span data-ttu-id="a9970-103">Crea una nuova risorsa ARM peering</span><span class="sxs-lookup"><span data-stu-id="a9970-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="a9970-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9970-104">SYNTAX</span></span>

### <span data-ttu-id="a9970-105">Exchange (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9970-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9970-106">ConvertLegacyApplicationing</span><span class="sxs-lookup"><span data-stu-id="a9970-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9970-107">Diretta</span><span class="sxs-lookup"><span data-stu-id="a9970-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9970-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9970-108">DESCRIPTION</span></span>
<span data-ttu-id="a9970-109">Crea un ARM peering per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a9970-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="a9970-110">Per altre informazioni sulla creazione di un oggetto connessione, vedere [New-AzDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) o [New-AzConnectioningExchangeConnectionObject.](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject)</span><span class="sxs-lookup"><span data-stu-id="a9970-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="a9970-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9970-111">EXAMPLES</span></span>

### <span data-ttu-id="a9970-112">Creare un nuovo peering diretto</span><span class="sxs-lookup"><span data-stu-id="a9970-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="a9970-113">Creare un nuovo peering diretto con una singola connessione nella struttura di Seattle usando PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="a9970-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="a9970-114">Creare un nuovo peering di Exchange</span><span class="sxs-lookup"><span data-stu-id="a9970-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a9970-115">Creare un nuovo peering di Exchange</span><span class="sxs-lookup"><span data-stu-id="a9970-115">Create a new exchange peering</span></span>

### <span data-ttu-id="a9970-116">Convertire il peering legacy in ARM peering</span><span class="sxs-lookup"><span data-stu-id="a9970-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="a9970-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9970-117">PARAMETERS</span></span>

### <span data-ttu-id="a9970-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9970-118">-AsJob</span></span>
<span data-ttu-id="a9970-119">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="a9970-119">Run in the background.</span></span>

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

### <span data-ttu-id="a9970-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9970-120">-DefaultProfile</span></span>
<span data-ttu-id="a9970-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9970-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9970-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="a9970-122">-DirectConnection</span></span>
<span data-ttu-id="a9970-123">Creare una nuova connessione diretta usando il comando New-AzExchangePeeringConnection eseguire la pipe e la connessione a questo comando.</span><span class="sxs-lookup"><span data-stu-id="a9970-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a9970-124">-ExchangeConnection</span></span>
<span data-ttu-id="a9970-125">Creare una nuova connessione Exchange usando il New-AzExchangePeeringConnection eseguire la pipe e la connessione a questo comando.</span><span class="sxs-lookup"><span data-stu-id="a9970-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9970-126">-InputObject</span></span>
<span data-ttu-id="a9970-127">Usare Get-AzLegacyPeering per recuperare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9970-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="a9970-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="a9970-129">Selezionare la rete Microsoft con cui si vuole aggiungere un peer.</span><span class="sxs-lookup"><span data-stu-id="a9970-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a9970-130">-Name</span></span>
<span data-ttu-id="a9970-131">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="a9970-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="a9970-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="a9970-133">ID risorsa Peer Asn. Usare Get-AzPeerAsn per recuperare l'ID.</span><span class="sxs-lookup"><span data-stu-id="a9970-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="a9970-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a9970-134">-PeeringLocation</span></span>
<span data-ttu-id="a9970-135">Posizione fisica diversa dall'area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9970-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="a9970-136">Usare Get-AzPeeringLocation -Kind \<kind\> use City name come chiave.</span><span class="sxs-lookup"><span data-stu-id="a9970-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9970-137">-ResourceGroupName</span></span>
<span data-ttu-id="a9970-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9970-138">The resource group name.</span></span>

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

### <span data-ttu-id="a9970-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="a9970-139">-Sku</span></span>
<span data-ttu-id="a9970-140">Selezionare Basic_Direct_Free o Premium_Direct_Free a meno che non venga esplicitamente specificato di selezionare un'altra opzione.</span><span class="sxs-lookup"><span data-stu-id="a9970-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9970-141">-Tag</span></span>
<span data-ttu-id="a9970-142">Tag da associare al servizio di peering Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9970-142">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9970-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9970-143">-Confirm</span></span>
<span data-ttu-id="a9970-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9970-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9970-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9970-145">-WhatIf</span></span>
<span data-ttu-id="a9970-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9970-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9970-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9970-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9970-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9970-148">CommonParameters</span></span>
<span data-ttu-id="a9970-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9970-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9970-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9970-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9970-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9970-151">INPUTS</span></span>

### <span data-ttu-id="a9970-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="a9970-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a9970-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9970-153">OUTPUTS</span></span>

### <span data-ttu-id="a9970-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="a9970-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a9970-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9970-155">NOTES</span></span>

## <span data-ttu-id="a9970-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9970-156">RELATED LINKS</span></span>
