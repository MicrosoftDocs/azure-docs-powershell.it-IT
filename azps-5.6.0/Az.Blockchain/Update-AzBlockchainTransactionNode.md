---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: 0a870fc286bce9b795d846dc1b8729dc4ddb25f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978893"
---
# <span data-ttu-id="433b6-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="433b6-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="433b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433b6-102">SYNOPSIS</span></span>
<span data-ttu-id="433b6-103">Aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-103">Update the transaction node.</span></span>

## <span data-ttu-id="433b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="433b6-104">SYNTAX</span></span>

### <span data-ttu-id="433b6-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="433b6-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="433b6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="433b6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="433b6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="433b6-107">DESCRIPTION</span></span>
<span data-ttu-id="433b6-108">Aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-108">Update the transaction node.</span></span>

## <span data-ttu-id="433b6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="433b6-109">EXAMPLES</span></span>

### <span data-ttu-id="433b6-110">Esempio 1: Aggiornare un nodo di trasposizione</span><span class="sxs-lookup"><span data-stu-id="433b6-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="433b6-111">Questo comando aggiorna un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="433b6-112">Esempio 2: Aggiornare un nodo di trasposizione</span><span class="sxs-lookup"><span data-stu-id="433b6-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="433b6-113">Questo comando aggiorna un nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="433b6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433b6-114">PARAMETERS</span></span>

### <span data-ttu-id="433b6-115">-MemberName</span><span class="sxs-lookup"><span data-stu-id="433b6-115">-BlockchainMemberName</span></span>
<span data-ttu-id="433b6-116">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="433b6-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="433b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433b6-117">-DefaultProfile</span></span>
<span data-ttu-id="433b6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="433b6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433b6-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="433b6-119">-FirewallRule</span></span>
<span data-ttu-id="433b6-120">Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="433b6-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="433b6-121">Per creare, vedere la sezione NOTE per le proprietà FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="433b6-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="433b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="433b6-122">-InputObject</span></span>
<span data-ttu-id="433b6-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="433b6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="433b6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="433b6-124">-Name</span></span>
<span data-ttu-id="433b6-125">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="433b6-126">-Password</span><span class="sxs-lookup"><span data-stu-id="433b6-126">-Password</span></span>
<span data-ttu-id="433b6-127">Imposta la password di base per l'autenticazione di base dell'endpoint dns del nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="433b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="433b6-129">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="433b6-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="433b6-130">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="433b6-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="433b6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="433b6-131">-SubscriptionId</span></span>
<span data-ttu-id="433b6-132">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="433b6-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="433b6-133">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="433b6-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="433b6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="433b6-134">-Confirm</span></span>
<span data-ttu-id="433b6-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="433b6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="433b6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="433b6-136">-WhatIf</span></span>
<span data-ttu-id="433b6-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="433b6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="433b6-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="433b6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="433b6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433b6-139">CommonParameters</span></span>
<span data-ttu-id="433b6-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433b6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433b6-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="433b6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433b6-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="433b6-142">INPUTS</span></span>

### <span data-ttu-id="433b6-143">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="433b6-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="433b6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="433b6-144">OUTPUTS</span></span>

### <span data-ttu-id="433b6-145">Microsoft.Azure.PowerShell.Cmdlets.Gateway.Models.Api20180601Preview.INode</span><span class="sxs-lookup"><span data-stu-id="433b6-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="433b6-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="433b6-146">NOTES</span></span>

<span data-ttu-id="433b6-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="433b6-147">ALIASES</span></span>

<span data-ttu-id="433b6-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="433b6-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="433b6-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="433b6-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="433b6-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="433b6-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="433b6-151">FIREWALLRULE <IFirewallRule[]>: ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="433b6-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="433b6-152">`[EndIPAddress <String>]`: ottiene o imposta l'indirizzo IP finale dell'intervallo delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="433b6-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="433b6-153">`[RuleName <String>]`: recupera o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="433b6-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="433b6-154">`[StartIPAddress <String>]`: ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="433b6-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="433b6-155">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="433b6-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="433b6-156">`[BlockchainMemberName <String>]`: nome di membro dell'team di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="433b6-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="433b6-157">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="433b6-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="433b6-158">`[Location <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="433b6-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="433b6-159">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="433b6-160">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="433b6-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="433b6-161">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="433b6-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="433b6-162">`[SubscriptionId <String>]`: ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="433b6-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="433b6-163">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="433b6-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="433b6-164">`[TransactionNodeName <String>]`: nome nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="433b6-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="433b6-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="433b6-165">RELATED LINKS</span></span>

