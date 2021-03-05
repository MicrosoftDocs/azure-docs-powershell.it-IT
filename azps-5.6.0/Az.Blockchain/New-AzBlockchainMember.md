---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: 15af3a6bb7e80020cd014bfbdd8ff944cafd187a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009357"
---
# <span data-ttu-id="d68cb-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="d68cb-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="d68cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d68cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d68cb-103">Creare un membro personale.</span><span class="sxs-lookup"><span data-stu-id="d68cb-103">Create a blockchain member.</span></span>

## <span data-ttu-id="d68cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d68cb-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d68cb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d68cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d68cb-106">Creare un membro personale.</span><span class="sxs-lookup"><span data-stu-id="d68cb-106">Create a blockchain member.</span></span>

## <span data-ttu-id="d68cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d68cb-107">EXAMPLES</span></span>

### <span data-ttu-id="d68cb-108">Esempio 1: Creare un nuovo membro member</span><span class="sxs-lookup"><span data-stu-id="d68cb-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="d68cb-109">Questo comando crea un nuovo membro di team.</span><span class="sxs-lookup"><span data-stu-id="d68cb-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="d68cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d68cb-110">PARAMETERS</span></span>

### <span data-ttu-id="d68cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d68cb-111">-AsJob</span></span>
<span data-ttu-id="d68cb-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d68cb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d68cb-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="d68cb-113">-Consortium</span></span>
<span data-ttu-id="d68cb-114">Ottiene o imposta il consorzio per il membro leso.</span><span class="sxs-lookup"><span data-stu-id="d68cb-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="d68cb-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d68cb-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="d68cb-116">Imposta la password dell'account di gestione del consorzio gestito.</span><span class="sxs-lookup"><span data-stu-id="d68cb-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="d68cb-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="d68cb-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="d68cb-118">Ottiene il nome visualizzato del membro del consorzio.</span><span class="sxs-lookup"><span data-stu-id="d68cb-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="d68cb-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="d68cb-119">-ConsortiumRole</span></span>
<span data-ttu-id="d68cb-120">Ottiene il ruolo del membro nel consorzio.</span><span class="sxs-lookup"><span data-stu-id="d68cb-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="d68cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68cb-121">-DefaultProfile</span></span>
<span data-ttu-id="d68cb-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d68cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68cb-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="d68cb-123">-FirewallRule</span></span>
<span data-ttu-id="d68cb-124">Ottiene o imposta le regole del firewall da creare, vedere la sezione NOTE per le proprietà FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d68cb-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d68cb-125">-Location</span><span class="sxs-lookup"><span data-stu-id="d68cb-125">-Location</span></span>
<span data-ttu-id="d68cb-126">Posizione GEO del servizio locale.</span><span class="sxs-lookup"><span data-stu-id="d68cb-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="d68cb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d68cb-127">-Name</span></span>
<span data-ttu-id="d68cb-128">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="d68cb-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="d68cb-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d68cb-129">-NoWait</span></span>
<span data-ttu-id="d68cb-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d68cb-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d68cb-131">-Password</span><span class="sxs-lookup"><span data-stu-id="d68cb-131">-Password</span></span>
<span data-ttu-id="d68cb-132">Imposta la password di autenticazione di base del membro member member.</span><span class="sxs-lookup"><span data-stu-id="d68cb-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="d68cb-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d68cb-133">-Protocol</span></span>
<span data-ttu-id="d68cb-134">Ottiene o imposta il protocollo protocol.</span><span class="sxs-lookup"><span data-stu-id="d68cb-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="d68cb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68cb-135">-ResourceGroupName</span></span>
<span data-ttu-id="d68cb-136">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d68cb-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d68cb-137">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="d68cb-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d68cb-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d68cb-138">-Sku</span></span>
<span data-ttu-id="d68cb-139">Ottiene o imposta il nome della SKU</span><span class="sxs-lookup"><span data-stu-id="d68cb-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="d68cb-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d68cb-140">-SkuTier</span></span>
<span data-ttu-id="d68cb-141">Ottiene o imposta il livello SKU</span><span class="sxs-lookup"><span data-stu-id="d68cb-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="d68cb-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d68cb-142">-SubscriptionId</span></span>
<span data-ttu-id="d68cb-143">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d68cb-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d68cb-144">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d68cb-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d68cb-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="d68cb-145">-Tag</span></span>
<span data-ttu-id="d68cb-146">Tag del servizio, ovvero un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d68cb-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="d68cb-147">-NodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d68cb-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="d68cb-148">Ottiene o imposta la capacità dei nodi.</span><span class="sxs-lookup"><span data-stu-id="d68cb-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="d68cb-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d68cb-149">-Confirm</span></span>
<span data-ttu-id="d68cb-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d68cb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d68cb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d68cb-151">-WhatIf</span></span>
<span data-ttu-id="d68cb-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d68cb-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d68cb-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d68cb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d68cb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68cb-154">CommonParameters</span></span>
<span data-ttu-id="d68cb-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d68cb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68cb-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d68cb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68cb-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="d68cb-157">INPUTS</span></span>

## <span data-ttu-id="d68cb-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d68cb-158">OUTPUTS</span></span>

### <span data-ttu-id="d68cb-159">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="d68cb-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="d68cb-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="d68cb-160">NOTES</span></span>

<span data-ttu-id="d68cb-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d68cb-161">ALIASES</span></span>

<span data-ttu-id="d68cb-162">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d68cb-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d68cb-163">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d68cb-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d68cb-164">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d68cb-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d68cb-165">FIREWALLRULE <IFirewallRule[]>: ottiene o imposta le regole del firewall</span><span class="sxs-lookup"><span data-stu-id="d68cb-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="d68cb-166">`[EndIPAddress <String>]`: ottiene o imposta l'indirizzo IP finale dell'intervallo delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="d68cb-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="d68cb-167">`[RuleName <String>]`: recupera o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="d68cb-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="d68cb-168">`[StartIPAddress <String>]`: ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="d68cb-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="d68cb-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d68cb-169">RELATED LINKS</span></span>

