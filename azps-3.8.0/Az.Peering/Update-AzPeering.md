---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022150"
---
# <span data-ttu-id="c934a-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c934a-101">Update-AzPeering</span></span>

## <span data-ttu-id="c934a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c934a-102">SYNOPSIS</span></span>
<span data-ttu-id="c934a-103">Imposta il peering.</span><span class="sxs-lookup"><span data-stu-id="c934a-103">Sets the Peering.</span></span> <span data-ttu-id="c934a-104">Usare questo comando in combinazione con `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="c934a-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="c934a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c934a-105">SYNTAX</span></span>

### <span data-ttu-id="c934a-106">DefaultExchange (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c934a-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c934a-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="c934a-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c934a-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="c934a-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c934a-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="c934a-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c934a-110">Diretto</span><span class="sxs-lookup"><span data-stu-id="c934a-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c934a-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="c934a-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c934a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c934a-112">DESCRIPTION</span></span>
<span data-ttu-id="c934a-113">Imposta l'oggetto PSPeering</span><span class="sxs-lookup"><span data-stu-id="c934a-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="c934a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c934a-114">EXAMPLES</span></span>

### <span data-ttu-id="c934a-115">Chiave di autenticazione MD5 di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c934a-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="c934a-116">Imposta la chiave di autenticazione MD5</span><span class="sxs-lookup"><span data-stu-id="c934a-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="c934a-117">Aggiornamento di UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="c934a-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c934a-118">Imposta l'opzione Usa per il servizio peering</span><span class="sxs-lookup"><span data-stu-id="c934a-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="c934a-119">Aggiornare l'indirizzo IPv4 per il peering di Exchange</span><span class="sxs-lookup"><span data-stu-id="c934a-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="c934a-120">Imposta l'indirizzo IPv4 per un peering di Exchange usando ResourceId</span><span class="sxs-lookup"><span data-stu-id="c934a-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="c934a-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c934a-121">PARAMETERS</span></span>

### <span data-ttu-id="c934a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c934a-122">-DefaultProfile</span></span>
<span data-ttu-id="c934a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c934a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c934a-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="c934a-124">-DirectConnection</span></span>
<span data-ttu-id="c934a-125">Creare un nuovo collegamento diretto usando la New-AzDirectPeeringConnectionObject e la pipe al comando.</span><span class="sxs-lookup"><span data-stu-id="c934a-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c934a-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="c934a-126">-ExchangeConnection</span></span>
<span data-ttu-id="c934a-127">Creare una nuova connessione di Exchange usando la New-AzExchangePeeringConnectionObject e la pipe al comando.</span><span class="sxs-lookup"><span data-stu-id="c934a-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c934a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c934a-128">-InputObject</span></span>
<span data-ttu-id="c934a-129">Oggetto peering</span><span class="sxs-lookup"><span data-stu-id="c934a-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c934a-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c934a-130">-Name</span></span>
<span data-ttu-id="c934a-131">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c934a-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c934a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c934a-132">-ResourceGroupName</span></span>
<span data-ttu-id="c934a-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c934a-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c934a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c934a-134">-ResourceId</span></span>
<span data-ttu-id="c934a-135">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c934a-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c934a-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c934a-136">-Confirm</span></span>
<span data-ttu-id="c934a-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c934a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c934a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c934a-138">-WhatIf</span></span>
<span data-ttu-id="c934a-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c934a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c934a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c934a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c934a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c934a-141">CommonParameters</span></span>
<span data-ttu-id="c934a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c934a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c934a-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c934a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c934a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c934a-144">INPUTS</span></span>

### <span data-ttu-id="c934a-145">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c934a-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c934a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c934a-146">System.String</span></span>

## <span data-ttu-id="c934a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c934a-147">OUTPUTS</span></span>

### <span data-ttu-id="c934a-148">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c934a-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="c934a-149">Note</span><span class="sxs-lookup"><span data-stu-id="c934a-149">NOTES</span></span>

## <span data-ttu-id="c934a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c934a-150">RELATED LINKS</span></span>
