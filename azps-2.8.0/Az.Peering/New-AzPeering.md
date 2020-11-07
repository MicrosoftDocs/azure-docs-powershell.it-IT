---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 341e2b4ad820b3a18e5515b54388ce517762d0ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855401"
---
# <span data-ttu-id="56712-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="56712-101">New-AzPeering</span></span>

## <span data-ttu-id="56712-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56712-102">SYNOPSIS</span></span>
<span data-ttu-id="56712-103">Crea una nuova risorsa peering ARM</span><span class="sxs-lookup"><span data-stu-id="56712-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="56712-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56712-104">SYNTAX</span></span>

### <span data-ttu-id="56712-105">Exchange (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56712-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56712-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="56712-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56712-107">Diretto</span><span class="sxs-lookup"><span data-stu-id="56712-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56712-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56712-108">DESCRIPTION</span></span>
<span data-ttu-id="56712-109">Crea un peering ARM per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="56712-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="56712-110">Per altre informazioni sulla creazione di un oggetto di connessione, vedere [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) o [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .</span><span class="sxs-lookup"><span data-stu-id="56712-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="56712-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56712-111">EXAMPLES</span></span>

### <span data-ttu-id="56712-112">Creare un nuovo peering diretto</span><span class="sxs-lookup"><span data-stu-id="56712-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="56712-113">Creare un nuovo peering diretto con una singola connessione presso la struttura di Seattle con PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="56712-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="56712-114">Creare un nuovo peering di Exchange</span><span class="sxs-lookup"><span data-stu-id="56712-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="56712-115">Creare un nuovo peering di Exchange</span><span class="sxs-lookup"><span data-stu-id="56712-115">Create a new exchange peering</span></span>

### <span data-ttu-id="56712-116">Convertire il peering legacy in peering ARM</span><span class="sxs-lookup"><span data-stu-id="56712-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="56712-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56712-117">PARAMETERS</span></span>

### <span data-ttu-id="56712-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56712-118">-AsJob</span></span>
<span data-ttu-id="56712-119">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="56712-119">Run in the background.</span></span>

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

### <span data-ttu-id="56712-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56712-120">-DefaultProfile</span></span>
<span data-ttu-id="56712-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56712-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56712-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="56712-122">-DirectConnection</span></span>
<span data-ttu-id="56712-123">Creare un nuovo collegamento diretto usando la New-AzExchangePeeringConnection e la pipe al comando.</span><span class="sxs-lookup"><span data-stu-id="56712-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="56712-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="56712-124">-ExchangeConnection</span></span>
<span data-ttu-id="56712-125">Creare una nuova connessione di Exchange usando la New-AzExchangePeeringConnection e la pipe al comando.</span><span class="sxs-lookup"><span data-stu-id="56712-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="56712-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56712-126">-InputObject</span></span>
<span data-ttu-id="56712-127">USA Get-AzLegacyPeering per recuperare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="56712-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="56712-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="56712-128">-Name</span></span>
<span data-ttu-id="56712-129">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="56712-129">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="56712-130">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="56712-130">-PeerAsnResourceId</span></span>
<span data-ttu-id="56712-131">ID risorsa ASN peer. usare Get-AzPeerAsn per recuperare l'ID.</span><span class="sxs-lookup"><span data-stu-id="56712-131">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="56712-132">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="56712-132">-PeeringLocation</span></span>
<span data-ttu-id="56712-133">Posizione fisica diversa dall'area di Azure.</span><span class="sxs-lookup"><span data-stu-id="56712-133">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="56712-134">Usa il tipo Get-AzPeeringLocation-kind \< \> use City Name come Key.</span><span class="sxs-lookup"><span data-stu-id="56712-134">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="56712-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56712-135">-ResourceGroupName</span></span>
<span data-ttu-id="56712-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56712-136">The resource group name.</span></span>

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

### <span data-ttu-id="56712-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="56712-137">-Sku</span></span>
<span data-ttu-id="56712-138">Selezionare Basic_Direct_Free o Premium_Direct_Free a meno che non venga detto esplicitamente di selezionare un'altra opzione.</span><span class="sxs-lookup"><span data-stu-id="56712-138">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="56712-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="56712-139">-Tag</span></span>
<span data-ttu-id="56712-140">Tag da associare al servizio peering Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56712-140">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="56712-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56712-141">-Confirm</span></span>
<span data-ttu-id="56712-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56712-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56712-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56712-143">-WhatIf</span></span>
<span data-ttu-id="56712-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56712-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56712-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56712-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56712-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56712-146">CommonParameters</span></span>
<span data-ttu-id="56712-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56712-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56712-148">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56712-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56712-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56712-149">INPUTS</span></span>

### <span data-ttu-id="56712-150">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="56712-150">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="56712-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56712-151">OUTPUTS</span></span>

### <span data-ttu-id="56712-152">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="56712-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="56712-153">Note</span><span class="sxs-lookup"><span data-stu-id="56712-153">NOTES</span></span>

## <span data-ttu-id="56712-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56712-154">RELATED LINKS</span></span>
