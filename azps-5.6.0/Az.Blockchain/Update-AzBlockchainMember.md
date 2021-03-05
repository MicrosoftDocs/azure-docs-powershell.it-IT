---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 833e660980d82c32667d166dbeed4520686d1124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975581"
---
# <span data-ttu-id="b204f-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="b204f-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="b204f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b204f-102">SYNOPSIS</span></span>
<span data-ttu-id="b204f-103">Aggiornare un membro del team.</span><span class="sxs-lookup"><span data-stu-id="b204f-103">Update a blockchain member.</span></span>

## <span data-ttu-id="b204f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b204f-104">SYNTAX</span></span>

### <span data-ttu-id="b204f-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b204f-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b204f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b204f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b204f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b204f-107">DESCRIPTION</span></span>
<span data-ttu-id="b204f-108">Aggiornare un membro del team.</span><span class="sxs-lookup"><span data-stu-id="b204f-108">Update a blockchain member.</span></span>

## <span data-ttu-id="b204f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b204f-109">EXAMPLES</span></span>

### <span data-ttu-id="b204f-110">Esempio 1: Aggiornare un membro member member di member member</span><span class="sxs-lookup"><span data-stu-id="b204f-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="b204f-111">Questo comando aggiorna un membro di member member.</span><span class="sxs-lookup"><span data-stu-id="b204f-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="b204f-112">Esempio 2: Aggiornare un membro member member di member member</span><span class="sxs-lookup"><span data-stu-id="b204f-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="b204f-113">Questo comando aggiorna un membro di member member.</span><span class="sxs-lookup"><span data-stu-id="b204f-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="b204f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b204f-114">PARAMETERS</span></span>

### <span data-ttu-id="b204f-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="b204f-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="b204f-116">Imposta la password dell'account di gestione del consorzio gestito.</span><span class="sxs-lookup"><span data-stu-id="b204f-116">Sets the managed consortium management account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b204f-117">-DefaultProfile</span></span>
<span data-ttu-id="b204f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b204f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b204f-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="b204f-119">-FirewallRule</span></span>
<span data-ttu-id="b204f-120">Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="b204f-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="b204f-121">Per creare, vedere la sezione NOTE per le proprietà FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b204f-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b204f-122">-InputObject</span></span>
<span data-ttu-id="b204f-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b204f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b204f-124">-Name</span></span>
<span data-ttu-id="b204f-125">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="b204f-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-126">-Password</span><span class="sxs-lookup"><span data-stu-id="b204f-126">-Password</span></span>
<span data-ttu-id="b204f-127">Imposta la password di base per l'autenticazione di base dell'endpoint dns del nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="b204f-127">Sets the transaction node dns endpoint basic auth password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b204f-128">-ResourceGroupName</span></span>
<span data-ttu-id="b204f-129">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b204f-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b204f-130">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b204f-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b204f-131">-SubscriptionId</span></span>
<span data-ttu-id="b204f-132">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b204f-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b204f-133">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b204f-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b204f-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="b204f-134">-Tag</span></span>
<span data-ttu-id="b204f-135">Tag del servizio, ovvero un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b204f-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="b204f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b204f-136">-Confirm</span></span>
<span data-ttu-id="b204f-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b204f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b204f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b204f-138">-WhatIf</span></span>
<span data-ttu-id="b204f-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b204f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b204f-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b204f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b204f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b204f-141">CommonParameters</span></span>
<span data-ttu-id="b204f-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b204f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b204f-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b204f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b204f-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="b204f-144">INPUTS</span></span>

### <span data-ttu-id="b204f-145">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="b204f-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="b204f-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b204f-146">OUTPUTS</span></span>

### <span data-ttu-id="b204f-147">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="b204f-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="b204f-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="b204f-148">NOTES</span></span>

<span data-ttu-id="b204f-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b204f-149">ALIASES</span></span>

<span data-ttu-id="b204f-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b204f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b204f-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b204f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b204f-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b204f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b204f-153">FIREWALLRULE <IFirewallRule[]>: ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="b204f-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="b204f-154">`[EndIPAddress <String>]`: ottiene o imposta l'indirizzo IP finale dell'intervallo delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="b204f-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="b204f-155">`[RuleName <String>]`: recupera o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="b204f-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="b204f-156">`[StartIPAddress <String>]`: ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="b204f-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="b204f-157">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b204f-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b204f-158">`[BlockchainMemberName <String>]`: nome di membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="b204f-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="b204f-159">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b204f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b204f-160">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b204f-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="b204f-161">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="b204f-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="b204f-162">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b204f-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b204f-163">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b204f-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b204f-164">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b204f-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b204f-165">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b204f-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="b204f-166">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="b204f-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="b204f-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b204f-167">RELATED LINKS</span></span>

