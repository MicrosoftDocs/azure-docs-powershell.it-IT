---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: d3da3e9dea25f872ce312b420cc8b36c7d17ffb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855362"
---
# <span data-ttu-id="a6c8c-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a6c8c-101">Update-AzPeering</span></span>

## <span data-ttu-id="a6c8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c8c-103">Imposta il peering.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-103">Sets the Peering.</span></span> <span data-ttu-id="a6c8c-104">Usare questo comando in combinazione con `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="a6c8c-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="a6c8c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6c8c-105">SYNTAX</span></span>

### <span data-ttu-id="a6c8c-106">DefaultExchange (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6c8c-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c8c-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="a6c8c-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c8c-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="a6c8c-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c8c-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="a6c8c-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c8c-110">Diretto</span><span class="sxs-lookup"><span data-stu-id="a6c8c-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c8c-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="a6c8c-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c8c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6c8c-112">DESCRIPTION</span></span>
<span data-ttu-id="a6c8c-113">Imposta l'oggetto PSPeering</span><span class="sxs-lookup"><span data-stu-id="a6c8c-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="a6c8c-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6c8c-114">EXAMPLES</span></span>

### <span data-ttu-id="a6c8c-115">Chiave di autenticazione MD5 di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a6c8c-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="a6c8c-116">Imposta la chiave di autenticazione MD5</span><span class="sxs-lookup"><span data-stu-id="a6c8c-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="a6c8c-117">Aggiornamento di UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="a6c8c-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="a6c8c-118">Imposta l'opzione Usa per il servizio peering</span><span class="sxs-lookup"><span data-stu-id="a6c8c-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="a6c8c-119">Aggiornare l'indirizzo IPv4 per il peering di Exchange</span><span class="sxs-lookup"><span data-stu-id="a6c8c-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="a6c8c-120">Imposta l'indirizzo IPv4 per un peering di Exchange usando ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c8c-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="a6c8c-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6c8c-121">PARAMETERS</span></span>

### <span data-ttu-id="a6c8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c8c-122">-DefaultProfile</span></span>
<span data-ttu-id="a6c8c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c8c-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="a6c8c-124">-DirectConnection</span></span>
<span data-ttu-id="a6c8c-125">Creare un nuovo collegamento diretto usando la New-AzDirectPeeringConnectionObject e la pipe al comando.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="a6c8c-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a6c8c-126">-ExchangeConnection</span></span>
<span data-ttu-id="a6c8c-127">Creare una nuova connessione di Exchange usando la New-AzExchangePeeringConnectionObject e la pipe al comando.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="a6c8c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c8c-128">-InputObject</span></span>
<span data-ttu-id="a6c8c-129">Oggetto peering</span><span class="sxs-lookup"><span data-stu-id="a6c8c-129">The Peering object</span></span> 

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

### <span data-ttu-id="a6c8c-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6c8c-130">-Name</span></span>
<span data-ttu-id="a6c8c-131">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a6c8c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c8c-132">-ResourceGroupName</span></span>
<span data-ttu-id="a6c8c-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-133">The resource group name.</span></span>

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

### <span data-ttu-id="a6c8c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c8c-134">-ResourceId</span></span>
<span data-ttu-id="a6c8c-135">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-135">The resource id string name.</span></span>

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

### <span data-ttu-id="a6c8c-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6c8c-136">-Confirm</span></span>
<span data-ttu-id="a6c8c-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c8c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c8c-138">-WhatIf</span></span>
<span data-ttu-id="a6c8c-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c8c-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c8c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c8c-141">CommonParameters</span></span>
<span data-ttu-id="a6c8c-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c8c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c8c-143">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6c8c-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c8c-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6c8c-144">INPUTS</span></span>

### <span data-ttu-id="a6c8c-145">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a6c8c-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a6c8c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c8c-146">System.String</span></span>

## <span data-ttu-id="a6c8c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6c8c-147">OUTPUTS</span></span>

### <span data-ttu-id="a6c8c-148">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a6c8c-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a6c8c-149">Note</span><span class="sxs-lookup"><span data-stu-id="a6c8c-149">NOTES</span></span>

## <span data-ttu-id="a6c8c-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6c8c-150">RELATED LINKS</span></span>
