---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200380"
---
# <span data-ttu-id="7eff6-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="7eff6-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="7eff6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eff6-102">SYNOPSIS</span></span>
<span data-ttu-id="7eff6-103">Aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-103">Update the transaction node.</span></span>

## <span data-ttu-id="7eff6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eff6-104">SYNTAX</span></span>

### <span data-ttu-id="7eff6-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7eff6-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7eff6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7eff6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7eff6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eff6-107">DESCRIPTION</span></span>
<span data-ttu-id="7eff6-108">Aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-108">Update the transaction node.</span></span>

## <span data-ttu-id="7eff6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eff6-109">EXAMPLES</span></span>

### <span data-ttu-id="7eff6-110">Esempio 1: aggiornare un nodo transcatione</span><span class="sxs-lookup"><span data-stu-id="7eff6-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="7eff6-111">Questo comando aggiorna un nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="7eff6-112">Esempio 2: aggiornare un nodo transcatione</span><span class="sxs-lookup"><span data-stu-id="7eff6-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="7eff6-113">Questo comando aggiorna un nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="7eff6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eff6-114">PARAMETERS</span></span>

### <span data-ttu-id="7eff6-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="7eff6-115">-BlockchainMemberName</span></span>
<span data-ttu-id="7eff6-116">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="7eff6-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="7eff6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eff6-117">-DefaultProfile</span></span>
<span data-ttu-id="7eff6-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7eff6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eff6-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7eff6-119">-FirewallRule</span></span>
<span data-ttu-id="7eff6-120">Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7eff6-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="7eff6-121">Per costruire, vedere la sezione Note per le proprietà di FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7eff6-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7eff6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eff6-122">-InputObject</span></span>
<span data-ttu-id="7eff6-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7eff6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7eff6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eff6-124">-Name</span></span>
<span data-ttu-id="7eff6-125">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-125">Transaction node name.</span></span>

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

### <span data-ttu-id="7eff6-126">-Password</span><span class="sxs-lookup"><span data-stu-id="7eff6-126">-Password</span></span>
<span data-ttu-id="7eff6-127">Imposta la password di autenticazione di base dell'endpoint DNS di Transaction node.</span><span class="sxs-lookup"><span data-stu-id="7eff6-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="7eff6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eff6-128">-ResourceGroupName</span></span>
<span data-ttu-id="7eff6-129">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eff6-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7eff6-130">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7eff6-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7eff6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7eff6-131">-SubscriptionId</span></span>
<span data-ttu-id="7eff6-132">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7eff6-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7eff6-133">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7eff6-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7eff6-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7eff6-134">-Confirm</span></span>
<span data-ttu-id="7eff6-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eff6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eff6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eff6-136">-WhatIf</span></span>
<span data-ttu-id="7eff6-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7eff6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eff6-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7eff6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eff6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eff6-139">CommonParameters</span></span>
<span data-ttu-id="7eff6-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eff6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eff6-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7eff6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eff6-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eff6-142">INPUTS</span></span>

### <span data-ttu-id="7eff6-143">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="7eff6-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="7eff6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eff6-144">OUTPUTS</span></span>

### <span data-ttu-id="7eff6-145">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="7eff6-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="7eff6-146">Note</span><span class="sxs-lookup"><span data-stu-id="7eff6-146">NOTES</span></span>

<span data-ttu-id="7eff6-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7eff6-147">ALIASES</span></span>

<span data-ttu-id="7eff6-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eff6-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7eff6-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7eff6-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7eff6-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7eff6-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7eff6-151">FIREWALLRULE <IFirewallRule [] >: Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7eff6-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="7eff6-152">`[EndIPAddress <String>]`: Ottiene o imposta l'indirizzo IP finale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7eff6-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="7eff6-153">`[RuleName <String>]`: Ottiene o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7eff6-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="7eff6-154">`[StartIPAddress <String>]`: Ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7eff6-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="7eff6-155">INPUTOBJECT <IBlockchainIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7eff6-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7eff6-156">`[BlockchainMemberName <String>]`: Nome membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="7eff6-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="7eff6-157">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7eff6-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7eff6-158">`[Location <String>]`: Nome posizione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="7eff6-159">`[OperationId <String>]`: ID operazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="7eff6-160">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eff6-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7eff6-161">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7eff6-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7eff6-162">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7eff6-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="7eff6-163">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7eff6-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="7eff6-164">`[TransactionNodeName <String>]`: Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="7eff6-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="7eff6-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eff6-165">RELATED LINKS</span></span>
