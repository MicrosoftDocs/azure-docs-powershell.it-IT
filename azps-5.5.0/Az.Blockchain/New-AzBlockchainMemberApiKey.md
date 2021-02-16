---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177951"
---
# <span data-ttu-id="aced9-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="aced9-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="aced9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aced9-102">SYNOPSIS</span></span>
<span data-ttu-id="aced9-103">Rigenerare le chiavi API per un membro member member di member member.</span><span class="sxs-lookup"><span data-stu-id="aced9-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="aced9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aced9-104">SYNTAX</span></span>

### <span data-ttu-id="aced9-105">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aced9-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aced9-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aced9-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aced9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aced9-107">DESCRIPTION</span></span>
<span data-ttu-id="aced9-108">Rigenerare le chiavi API per un membro member member di member member.</span><span class="sxs-lookup"><span data-stu-id="aced9-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="aced9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aced9-109">EXAMPLES</span></span>

### <span data-ttu-id="aced9-110">Esempio 1: Rigenerare le chiavi API per un membro member usando name</span><span class="sxs-lookup"><span data-stu-id="aced9-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="aced9-111">Questo comando rigenera le chiavi API per un membro member usando name, resource group.</span><span class="sxs-lookup"><span data-stu-id="aced9-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="aced9-112">Esempio 2: Rigenerare le chiavi API per un membro personale usando idenity</span><span class="sxs-lookup"><span data-stu-id="aced9-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="aced9-113">Questo comando rigenera le chiavi API per un membro member usando identity.</span><span class="sxs-lookup"><span data-stu-id="aced9-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="aced9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aced9-114">PARAMETERS</span></span>

### <span data-ttu-id="aced9-115">-MemberName</span><span class="sxs-lookup"><span data-stu-id="aced9-115">-BlockchainMemberName</span></span>
<span data-ttu-id="aced9-116">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="aced9-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aced9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aced9-117">-DefaultProfile</span></span>
<span data-ttu-id="aced9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aced9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aced9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aced9-119">-InputObject</span></span>
<span data-ttu-id="aced9-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="aced9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aced9-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="aced9-121">-KeyName</span></span>
<span data-ttu-id="aced9-122">Ottiene o imposta il nome della chiave API.</span><span class="sxs-lookup"><span data-stu-id="aced9-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="aced9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aced9-123">-ResourceGroupName</span></span>
<span data-ttu-id="aced9-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="aced9-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aced9-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="aced9-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aced9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aced9-126">-SubscriptionId</span></span>
<span data-ttu-id="aced9-127">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aced9-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aced9-128">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="aced9-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aced9-129">-Value</span><span class="sxs-lookup"><span data-stu-id="aced9-129">-Value</span></span>
<span data-ttu-id="aced9-130">Ottiene o imposta il valore della chiave API.</span><span class="sxs-lookup"><span data-stu-id="aced9-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="aced9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aced9-131">-Confirm</span></span>
<span data-ttu-id="aced9-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aced9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aced9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aced9-133">-WhatIf</span></span>
<span data-ttu-id="aced9-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aced9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aced9-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aced9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aced9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aced9-136">CommonParameters</span></span>
<span data-ttu-id="aced9-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aced9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aced9-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aced9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aced9-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="aced9-139">INPUTS</span></span>

### <span data-ttu-id="aced9-140">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="aced9-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="aced9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aced9-141">OUTPUTS</span></span>

### <span data-ttu-id="aced9-142">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="aced9-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="aced9-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="aced9-143">NOTES</span></span>

<span data-ttu-id="aced9-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aced9-144">ALIASES</span></span>

<span data-ttu-id="aced9-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="aced9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aced9-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="aced9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aced9-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aced9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aced9-148">INPUTOBJECT <IBlockchainIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="aced9-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aced9-149">`[BlockchainMemberName <String>]`: nome membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="aced9-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="aced9-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="aced9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aced9-151">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="aced9-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="aced9-152">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="aced9-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="aced9-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="aced9-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="aced9-154">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="aced9-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="aced9-155">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aced9-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="aced9-156">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="aced9-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="aced9-157">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="aced9-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="aced9-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aced9-158">RELATED LINKS</span></span>

