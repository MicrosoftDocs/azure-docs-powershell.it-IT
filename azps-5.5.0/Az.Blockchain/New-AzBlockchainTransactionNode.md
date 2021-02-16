---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177950"
---
# <span data-ttu-id="7afeb-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="7afeb-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="7afeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7afeb-102">SYNOPSIS</span></span>
<span data-ttu-id="7afeb-103">Creare o aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7afeb-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="7afeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7afeb-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7afeb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7afeb-105">DESCRIPTION</span></span>
<span data-ttu-id="7afeb-106">Creare o aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7afeb-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="7afeb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7afeb-107">EXAMPLES</span></span>

### <span data-ttu-id="7afeb-108">Esempio 1: Creare un nodo di transazione node di una piattaforma</span><span class="sxs-lookup"><span data-stu-id="7afeb-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="7afeb-109">Questo comando crea un nodo di transazione di microsoft Transaction.</span><span class="sxs-lookup"><span data-stu-id="7afeb-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="7afeb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7afeb-110">PARAMETERS</span></span>

### <span data-ttu-id="7afeb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7afeb-111">-AsJob</span></span>
<span data-ttu-id="7afeb-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7afeb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7afeb-113">-MemberName</span><span class="sxs-lookup"><span data-stu-id="7afeb-113">-BlockchainMemberName</span></span>
<span data-ttu-id="7afeb-114">Nome di un membro del Team Team.</span><span class="sxs-lookup"><span data-stu-id="7afeb-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="7afeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afeb-115">-DefaultProfile</span></span>
<span data-ttu-id="7afeb-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7afeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7afeb-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7afeb-117">-FirewallRule</span></span>
<span data-ttu-id="7afeb-118">Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7afeb-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="7afeb-119">Per creare, vedere la sezione NOTE per le proprietà FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7afeb-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7afeb-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7afeb-120">-Location</span></span>
<span data-ttu-id="7afeb-121">Ottiene o imposta la posizione del nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="7afeb-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="7afeb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7afeb-122">-Name</span></span>
<span data-ttu-id="7afeb-123">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="7afeb-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afeb-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7afeb-124">-NoWait</span></span>
<span data-ttu-id="7afeb-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7afeb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7afeb-126">-Password</span><span class="sxs-lookup"><span data-stu-id="7afeb-126">-Password</span></span>
<span data-ttu-id="7afeb-127">Imposta la password di base per l'autenticazione di base dell'endpoint dns del nodo di transazione.</span><span class="sxs-lookup"><span data-stu-id="7afeb-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="7afeb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7afeb-128">-ResourceGroupName</span></span>
<span data-ttu-id="7afeb-129">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7afeb-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7afeb-130">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7afeb-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7afeb-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7afeb-131">-SubscriptionId</span></span>
<span data-ttu-id="7afeb-132">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7afeb-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7afeb-133">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7afeb-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7afeb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7afeb-134">-Confirm</span></span>
<span data-ttu-id="7afeb-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7afeb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7afeb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7afeb-136">-WhatIf</span></span>
<span data-ttu-id="7afeb-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7afeb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7afeb-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7afeb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7afeb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afeb-139">CommonParameters</span></span>
<span data-ttu-id="7afeb-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7afeb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afeb-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7afeb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afeb-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="7afeb-142">INPUTS</span></span>

## <span data-ttu-id="7afeb-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7afeb-143">OUTPUTS</span></span>

### <span data-ttu-id="7afeb-144">Microsoft.Azure.PowerShell.Cmdlets.Cmdlets.Gateway.Models.Api20180601Preview.INode</span><span class="sxs-lookup"><span data-stu-id="7afeb-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="7afeb-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="7afeb-145">NOTES</span></span>

<span data-ttu-id="7afeb-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7afeb-146">ALIASES</span></span>

<span data-ttu-id="7afeb-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7afeb-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7afeb-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7afeb-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7afeb-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7afeb-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7afeb-150">FIREWALLRULE <IFirewallRule[]>: ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7afeb-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="7afeb-151">`[EndIPAddress <String>]`: ottiene o imposta l'indirizzo IP finale dell'intervallo delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7afeb-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="7afeb-152">`[RuleName <String>]`: recupera o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7afeb-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="7afeb-153">`[StartIPAddress <String>]`: ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="7afeb-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="7afeb-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7afeb-154">RELATED LINKS</span></span>

