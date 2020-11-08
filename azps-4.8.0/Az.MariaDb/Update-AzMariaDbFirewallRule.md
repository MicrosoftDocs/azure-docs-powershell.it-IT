---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189585"
---
# <span data-ttu-id="f16ab-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f16ab-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="f16ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f16ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f16ab-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="f16ab-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f16ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f16ab-104">SYNTAX</span></span>

### <span data-ttu-id="f16ab-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f16ab-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f16ab-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f16ab-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f16ab-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f16ab-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f16ab-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f16ab-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f16ab-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f16ab-109">DESCRIPTION</span></span>
<span data-ttu-id="f16ab-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="f16ab-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f16ab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f16ab-111">EXAMPLES</span></span>

### <span data-ttu-id="f16ab-112">Esempio 1: aggiornare la regola del firewall di MariaDB</span><span class="sxs-lookup"><span data-stu-id="f16ab-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="f16ab-113">Questo comando aggiorna una regola del firewall MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f16ab-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="f16ab-114">Esempio 2: aggiornare la regola del firewall di MariaDB in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="f16ab-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="f16ab-115">Il cmdlet aggiorna la regola del firewall MariaDB in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="f16ab-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="f16ab-116">Esempio 3: aggiornare la regola del firewall di MariaDB per-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="f16ab-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="f16ab-117">Il cmdlet aggiorna la regola del firewall di MariaDB per-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="f16ab-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="f16ab-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f16ab-118">PARAMETERS</span></span>

### <span data-ttu-id="f16ab-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f16ab-119">-AsJob</span></span>
<span data-ttu-id="f16ab-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f16ab-120">Run the command as a job</span></span>

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

### <span data-ttu-id="f16ab-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f16ab-121">-ClientIPAddress</span></span>
<span data-ttu-id="f16ab-122">Il client ha specificato un singolo IP della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f16ab-123">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="f16ab-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f16ab-124">-DefaultProfile</span></span>
<span data-ttu-id="f16ab-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f16ab-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f16ab-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="f16ab-126">-EndIPAddress</span></span>
<span data-ttu-id="f16ab-127">Indirizzo IP finale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f16ab-128">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="f16ab-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f16ab-129">-InputObject</span></span>
<span data-ttu-id="f16ab-130">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f16ab-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f16ab-131">-Name</span></span>
<span data-ttu-id="f16ab-132">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="f16ab-133">-NoWait</span></span>
<span data-ttu-id="f16ab-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f16ab-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f16ab-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f16ab-135">-ResourceGroupName</span></span>
<span data-ttu-id="f16ab-136">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f16ab-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f16ab-137">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="f16ab-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-138">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f16ab-138">-ServerName</span></span>
<span data-ttu-id="f16ab-139">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="f16ab-140">-StartIPAddress</span></span>
<span data-ttu-id="f16ab-141">Indirizzo IP iniziale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f16ab-142">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="f16ab-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f16ab-143">-SubscriptionId</span></span>
<span data-ttu-id="f16ab-144">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="f16ab-144">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16ab-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f16ab-145">-Confirm</span></span>
<span data-ttu-id="f16ab-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f16ab-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f16ab-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f16ab-147">-WhatIf</span></span>
<span data-ttu-id="f16ab-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f16ab-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f16ab-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f16ab-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f16ab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f16ab-150">CommonParameters</span></span>
<span data-ttu-id="f16ab-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f16ab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f16ab-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f16ab-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f16ab-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f16ab-153">INPUTS</span></span>

### <span data-ttu-id="f16ab-154">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f16ab-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f16ab-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f16ab-155">OUTPUTS</span></span>

### <span data-ttu-id="f16ab-156">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f16ab-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="f16ab-157">Note</span><span class="sxs-lookup"><span data-stu-id="f16ab-157">NOTES</span></span>

<span data-ttu-id="f16ab-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f16ab-158">ALIASES</span></span>

<span data-ttu-id="f16ab-159">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f16ab-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f16ab-160">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f16ab-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f16ab-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f16ab-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f16ab-162">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f16ab-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f16ab-163">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f16ab-164">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="f16ab-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f16ab-165">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f16ab-166">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f16ab-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f16ab-167">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="f16ab-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f16ab-168">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f16ab-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f16ab-169">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="f16ab-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f16ab-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f16ab-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f16ab-171">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="f16ab-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f16ab-172">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="f16ab-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f16ab-173">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f16ab-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f16ab-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f16ab-174">RELATED LINKS</span></span>

