---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203004"
---
# <span data-ttu-id="af061-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="af061-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="af061-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af061-102">SYNOPSIS</span></span>
<span data-ttu-id="af061-103">Creare o aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="af061-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="af061-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af061-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af061-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af061-105">DESCRIPTION</span></span>
<span data-ttu-id="af061-106">Creare o aggiornare il nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="af061-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="af061-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af061-107">EXAMPLES</span></span>

### <span data-ttu-id="af061-108">Esempio 1: creare un nodo delle transazioni blockchain</span><span class="sxs-lookup"><span data-stu-id="af061-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="af061-109">Questo comando crea un nodo transazione blockchain.</span><span class="sxs-lookup"><span data-stu-id="af061-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="af061-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af061-110">PARAMETERS</span></span>

### <span data-ttu-id="af061-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af061-111">-AsJob</span></span>
<span data-ttu-id="af061-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="af061-112">Run the command as a job</span></span>

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

### <span data-ttu-id="af061-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="af061-113">-BlockchainMemberName</span></span>
<span data-ttu-id="af061-114">Nome del membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="af061-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="af061-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af061-115">-DefaultProfile</span></span>
<span data-ttu-id="af061-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af061-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af061-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="af061-117">-FirewallRule</span></span>
<span data-ttu-id="af061-118">Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="af061-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="af061-119">Per costruire, vedere la sezione Note per le proprietà di FIREWALLRULE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="af061-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="af061-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="af061-120">-Location</span></span>
<span data-ttu-id="af061-121">Ottiene o imposta la posizione del nodo della transazione.</span><span class="sxs-lookup"><span data-stu-id="af061-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="af061-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="af061-122">-Name</span></span>
<span data-ttu-id="af061-123">Nome nodo transazione.</span><span class="sxs-lookup"><span data-stu-id="af061-123">Transaction node name.</span></span>

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

### <span data-ttu-id="af061-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="af061-124">-NoWait</span></span>
<span data-ttu-id="af061-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="af061-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af061-126">-Password</span><span class="sxs-lookup"><span data-stu-id="af061-126">-Password</span></span>
<span data-ttu-id="af061-127">Imposta la password di autenticazione di base dell'endpoint DNS di Transaction node.</span><span class="sxs-lookup"><span data-stu-id="af061-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="af061-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af061-128">-ResourceGroupName</span></span>
<span data-ttu-id="af061-129">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="af061-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="af061-130">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="af061-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="af061-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af061-131">-SubscriptionId</span></span>
<span data-ttu-id="af061-132">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="af061-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="af061-133">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="af061-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="af061-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af061-134">-Confirm</span></span>
<span data-ttu-id="af061-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af061-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af061-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af061-136">-WhatIf</span></span>
<span data-ttu-id="af061-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af061-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af061-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af061-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af061-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af061-139">CommonParameters</span></span>
<span data-ttu-id="af061-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af061-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af061-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af061-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af061-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af061-142">INPUTS</span></span>

## <span data-ttu-id="af061-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af061-143">OUTPUTS</span></span>

### <span data-ttu-id="af061-144">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="af061-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="af061-145">Note</span><span class="sxs-lookup"><span data-stu-id="af061-145">NOTES</span></span>

<span data-ttu-id="af061-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="af061-146">ALIASES</span></span>

<span data-ttu-id="af061-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af061-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af061-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="af061-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af061-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af061-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af061-150">FIREWALLRULE <IFirewallRule [] >: Ottiene o imposta le regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="af061-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="af061-151">`[EndIPAddress <String>]`: Ottiene o imposta l'indirizzo IP finale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="af061-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="af061-152">`[RuleName <String>]`: Ottiene o imposta il nome delle regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="af061-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="af061-153">`[StartIPAddress <String>]`: Ottiene o imposta l'indirizzo IP iniziale dell'intervallo di regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="af061-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="af061-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af061-154">RELATED LINKS</span></span>

