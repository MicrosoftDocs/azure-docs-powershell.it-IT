---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032617"
---
# <span data-ttu-id="fd88e-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="fd88e-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="fd88e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd88e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd88e-103">Aggiornare un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="fd88e-103">Update a blockchain member.</span></span>

## <span data-ttu-id="fd88e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd88e-104">SYNTAX</span></span>

### <span data-ttu-id="fd88e-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd88e-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fd88e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fd88e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fd88e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd88e-107">DESCRIPTION</span></span>
<span data-ttu-id="fd88e-108">Aggiornare un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="fd88e-108">Update a blockchain member.</span></span>

## <span data-ttu-id="fd88e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd88e-109">EXAMPLES</span></span>

### <span data-ttu-id="fd88e-110">Esempio 1: aggiornare un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="fd88e-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="fd88e-111">Questo comando aggiorna un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="fd88e-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="fd88e-112">Esempio 2: aggiornare un membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="fd88e-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="fd88e-113">Questo comando aggiorna un membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="fd88e-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="fd88e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd88e-114">PARAMETERS</span></span>

### <span data-ttu-id="fd88e-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="fd88e-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="fd88e-116">Imposta la password dell'account di gestione consorziale gestito.</span><span class="sxs-lookup"><span data-stu-id="fd88e-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="fd88e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd88e-117">-DefaultProfile</span></span>
<span data-ttu-id="fd88e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd88e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd88e-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fd88e-119">-FirewallRule</span></span>
<span data-ttu-id="fd88e-120">Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="fd88e-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="fd88e-121">Per costruire, vedere la sezione Note per le proprietà di FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fd88e-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd88e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd88e-122">-InputObject</span></span>
<span data-ttu-id="fd88e-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fd88e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd88e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd88e-124">-Name</span></span>
<span data-ttu-id="fd88e-125">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="fd88e-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="fd88e-126">-Password</span><span class="sxs-lookup"><span data-stu-id="fd88e-126">-Password</span></span>
<span data-ttu-id="fd88e-127">Imposta la password di autenticazione di base dell'endpoint DNS di Transaction node.</span><span class="sxs-lookup"><span data-stu-id="fd88e-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="fd88e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd88e-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd88e-129">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd88e-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fd88e-130">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="fd88e-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fd88e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd88e-131">-SubscriptionId</span></span>
<span data-ttu-id="fd88e-132">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd88e-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd88e-133">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fd88e-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd88e-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd88e-134">-Tag</span></span>
<span data-ttu-id="fd88e-135">Tag del servizio che è un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd88e-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="fd88e-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd88e-136">-Confirm</span></span>
<span data-ttu-id="fd88e-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd88e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd88e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd88e-138">-WhatIf</span></span>
<span data-ttu-id="fd88e-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd88e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd88e-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd88e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd88e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd88e-141">CommonParameters</span></span>
<span data-ttu-id="fd88e-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd88e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd88e-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd88e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd88e-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd88e-144">INPUTS</span></span>

### <span data-ttu-id="fd88e-145">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="fd88e-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="fd88e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd88e-146">OUTPUTS</span></span>

### <span data-ttu-id="fd88e-147">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="fd88e-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="fd88e-148">Note</span><span class="sxs-lookup"><span data-stu-id="fd88e-148">NOTES</span></span>

<span data-ttu-id="fd88e-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fd88e-149">ALIASES</span></span>

<span data-ttu-id="fd88e-150">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd88e-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd88e-151">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fd88e-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd88e-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd88e-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd88e-153">FIREWALLRULE <IFirewallRule [] >: Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="fd88e-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="fd88e-154">`[EndIPAddress <String>]`: Ottiene o imposta l'indirizzo IP finale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="fd88e-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="fd88e-155">`[RuleName <String>]`: Ottiene o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="fd88e-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="fd88e-156">`[StartIPAddress <String>]`: Ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="fd88e-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="fd88e-157">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="fd88e-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd88e-158">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="fd88e-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="fd88e-159">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="fd88e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd88e-160">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="fd88e-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="fd88e-161">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="fd88e-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="fd88e-162">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd88e-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fd88e-163">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="fd88e-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fd88e-164">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd88e-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="fd88e-165">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fd88e-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="fd88e-166">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="fd88e-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="fd88e-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd88e-167">RELATED LINKS</span></span>

