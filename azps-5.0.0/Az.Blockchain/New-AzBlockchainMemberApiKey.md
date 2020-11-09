---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301584"
---
# <span data-ttu-id="ac88f-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="ac88f-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="ac88f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac88f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac88f-103">Rigenerare le chiavi dell'API per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="ac88f-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="ac88f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac88f-104">SYNTAX</span></span>

### <span data-ttu-id="ac88f-105">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac88f-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac88f-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac88f-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac88f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac88f-107">DESCRIPTION</span></span>
<span data-ttu-id="ac88f-108">Rigenerare le chiavi dell'API per un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="ac88f-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="ac88f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac88f-109">EXAMPLES</span></span>

### <span data-ttu-id="ac88f-110">Esempio 1: rigenerare le chiavi API per un membro di blockchain usando Name</span><span class="sxs-lookup"><span data-stu-id="ac88f-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="ac88f-111">Questo comando rigenera le chiavi API per un membro di blockchain usando nome, gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="ac88f-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="ac88f-112">Esempio 2: rigenerare le chiavi API per un membro di blockchain usando l'identità</span><span class="sxs-lookup"><span data-stu-id="ac88f-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="ac88f-113">Questo comando rigenera le chiavi API per un membro di blockchain usando l'identità.</span><span class="sxs-lookup"><span data-stu-id="ac88f-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="ac88f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac88f-114">PARAMETERS</span></span>

### <span data-ttu-id="ac88f-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="ac88f-115">-BlockchainMemberName</span></span>
<span data-ttu-id="ac88f-116">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="ac88f-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="ac88f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac88f-117">-DefaultProfile</span></span>
<span data-ttu-id="ac88f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac88f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac88f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac88f-119">-InputObject</span></span>
<span data-ttu-id="ac88f-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ac88f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac88f-121">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ac88f-121">-KeyName</span></span>
<span data-ttu-id="ac88f-122">Ottiene o imposta il nome della chiave dell'API.</span><span class="sxs-lookup"><span data-stu-id="ac88f-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="ac88f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac88f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac88f-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ac88f-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ac88f-125">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ac88f-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ac88f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac88f-126">-SubscriptionId</span></span>
<span data-ttu-id="ac88f-127">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac88f-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac88f-128">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ac88f-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ac88f-129">-Valore</span><span class="sxs-lookup"><span data-stu-id="ac88f-129">-Value</span></span>
<span data-ttu-id="ac88f-130">Ottiene o imposta il valore della chiave API.</span><span class="sxs-lookup"><span data-stu-id="ac88f-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="ac88f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac88f-131">-Confirm</span></span>
<span data-ttu-id="ac88f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac88f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac88f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac88f-133">-WhatIf</span></span>
<span data-ttu-id="ac88f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac88f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac88f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac88f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac88f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac88f-136">CommonParameters</span></span>
<span data-ttu-id="ac88f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac88f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac88f-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac88f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac88f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac88f-139">INPUTS</span></span>

### <span data-ttu-id="ac88f-140">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="ac88f-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="ac88f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac88f-141">OUTPUTS</span></span>

### <span data-ttu-id="ac88f-142">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="ac88f-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="ac88f-143">Note</span><span class="sxs-lookup"><span data-stu-id="ac88f-143">NOTES</span></span>

<span data-ttu-id="ac88f-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac88f-144">ALIASES</span></span>

<span data-ttu-id="ac88f-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac88f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac88f-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ac88f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac88f-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac88f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac88f-148">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ac88f-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac88f-149">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="ac88f-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="ac88f-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ac88f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac88f-151">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="ac88f-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="ac88f-152">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="ac88f-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="ac88f-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ac88f-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ac88f-154">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ac88f-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ac88f-155">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac88f-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ac88f-156">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ac88f-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="ac88f-157">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="ac88f-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="ac88f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac88f-158">RELATED LINKS</span></span>

