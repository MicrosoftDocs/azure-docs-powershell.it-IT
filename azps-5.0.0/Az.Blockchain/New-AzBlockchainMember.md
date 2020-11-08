---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203006"
---
# <span data-ttu-id="be3e4-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="be3e4-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="be3e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="be3e4-103">Creare un membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-103">Create a blockchain member.</span></span>

## <span data-ttu-id="be3e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be3e4-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be3e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be3e4-105">DESCRIPTION</span></span>
<span data-ttu-id="be3e4-106">Creare un membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-106">Create a blockchain member.</span></span>

## <span data-ttu-id="be3e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be3e4-107">EXAMPLES</span></span>

### <span data-ttu-id="be3e4-108">Esempio 1: creare un nuovo membro di blockchain</span><span class="sxs-lookup"><span data-stu-id="be3e4-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="be3e4-109">Questo comando crea un nuovo membro di blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="be3e4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be3e4-110">PARAMETERS</span></span>

### <span data-ttu-id="be3e4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be3e4-111">-AsJob</span></span>
<span data-ttu-id="be3e4-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="be3e4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="be3e4-113">-Consorzio</span><span class="sxs-lookup"><span data-stu-id="be3e4-113">-Consortium</span></span>
<span data-ttu-id="be3e4-114">Ottiene o imposta il Consorzio per il membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="be3e4-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="be3e4-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="be3e4-116">Imposta la password dell'account di gestione consorziale gestito.</span><span class="sxs-lookup"><span data-stu-id="be3e4-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="be3e4-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="be3e4-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="be3e4-118">Ottiene il nome visualizzato del membro nel Consorzio.</span><span class="sxs-lookup"><span data-stu-id="be3e4-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="be3e4-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="be3e4-119">-ConsortiumRole</span></span>
<span data-ttu-id="be3e4-120">Ottiene il ruolo del membro nel Consorzio.</span><span class="sxs-lookup"><span data-stu-id="be3e4-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="be3e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3e4-121">-DefaultProfile</span></span>
<span data-ttu-id="be3e4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be3e4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be3e4-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="be3e4-123">-FirewallRule</span></span>
<span data-ttu-id="be3e4-124">Ottiene o imposta regole del firewall da creare, vedere la sezione Note per le proprietà di FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="be3e4-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="be3e4-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="be3e4-125">-Location</span></span>
<span data-ttu-id="be3e4-126">Posizione GEO del servizio blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="be3e4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="be3e4-127">-Name</span></span>
<span data-ttu-id="be3e4-128">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3e4-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="be3e4-129">-NoWait</span></span>
<span data-ttu-id="be3e4-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="be3e4-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be3e4-131">-Password</span><span class="sxs-lookup"><span data-stu-id="be3e4-131">-Password</span></span>
<span data-ttu-id="be3e4-132">Imposta la password di autenticazione di base del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="be3e4-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="be3e4-133">-Protocol</span></span>
<span data-ttu-id="be3e4-134">Ottiene o imposta il protocollo blockchain.</span><span class="sxs-lookup"><span data-stu-id="be3e4-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3e4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be3e4-135">-ResourceGroupName</span></span>
<span data-ttu-id="be3e4-136">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be3e4-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="be3e4-137">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="be3e4-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="be3e4-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="be3e4-138">-Sku</span></span>
<span data-ttu-id="be3e4-139">Ottiene o imposta il nome Usk</span><span class="sxs-lookup"><span data-stu-id="be3e4-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="be3e4-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="be3e4-140">-SkuTier</span></span>
<span data-ttu-id="be3e4-141">Ottiene o imposta il livello SKU</span><span class="sxs-lookup"><span data-stu-id="be3e4-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="be3e4-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be3e4-142">-SubscriptionId</span></span>
<span data-ttu-id="be3e4-143">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be3e4-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="be3e4-144">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="be3e4-144">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3e4-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="be3e4-145">-Tag</span></span>
<span data-ttu-id="be3e4-146">Tag del servizio che è un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be3e4-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="be3e4-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="be3e4-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="be3e4-148">Ottiene o imposta la capacità dei nodi.</span><span class="sxs-lookup"><span data-stu-id="be3e4-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="be3e4-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be3e4-149">-Confirm</span></span>
<span data-ttu-id="be3e4-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be3e4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be3e4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be3e4-151">-WhatIf</span></span>
<span data-ttu-id="be3e4-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be3e4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be3e4-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be3e4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be3e4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3e4-154">CommonParameters</span></span>
<span data-ttu-id="be3e4-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be3e4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3e4-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be3e4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3e4-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be3e4-157">INPUTS</span></span>

## <span data-ttu-id="be3e4-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be3e4-158">OUTPUTS</span></span>

### <span data-ttu-id="be3e4-159">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="be3e4-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="be3e4-160">Note</span><span class="sxs-lookup"><span data-stu-id="be3e4-160">NOTES</span></span>

<span data-ttu-id="be3e4-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="be3e4-161">ALIASES</span></span>

<span data-ttu-id="be3e4-162">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be3e4-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be3e4-163">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="be3e4-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be3e4-164">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be3e4-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be3e4-165">FIREWALLRULE <IFirewallRule [] >: Ottiene o imposta regole del firewall</span><span class="sxs-lookup"><span data-stu-id="be3e4-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="be3e4-166">`[EndIPAddress <String>]`: Ottiene o imposta l'indirizzo IP finale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="be3e4-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="be3e4-167">`[RuleName <String>]`: Ottiene o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="be3e4-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="be3e4-168">`[StartIPAddress <String>]`: Ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="be3e4-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="be3e4-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be3e4-169">RELATED LINKS</span></span>

