---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: fe6ef1a5193119c4778d18c39a7ecff98354cf89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206243"
---
# <span data-ttu-id="42897-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="42897-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="42897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42897-102">SYNOPSIS</span></span>
<span data-ttu-id="42897-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="42897-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="42897-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42897-104">SYNTAX</span></span>

### <span data-ttu-id="42897-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42897-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="42897-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="42897-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="42897-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="42897-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="42897-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="42897-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="42897-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42897-109">DESCRIPTION</span></span>
<span data-ttu-id="42897-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="42897-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="42897-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42897-111">EXAMPLES</span></span>

### <span data-ttu-id="42897-112">Esempio 1: Aggiornare la regola del firewall PostgreSql in base al nome</span><span class="sxs-lookup"><span data-stu-id="42897-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="42897-113">Questo cmdlet aggiorna la regola del firewall PostgreSql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="42897-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="42897-114">Esempio 2: Aggiornare la regola del firewall PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="42897-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="42897-115">Questi cmdlet aggiornano la regola del firewall PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="42897-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="42897-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42897-116">PARAMETERS</span></span>

### <span data-ttu-id="42897-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42897-117">-AsJob</span></span>
<span data-ttu-id="42897-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="42897-118">Run the command as a job</span></span>

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

### <span data-ttu-id="42897-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="42897-119">-ClientIPAddress</span></span>
<span data-ttu-id="42897-120">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="42897-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="42897-121">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="42897-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="42897-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42897-122">-DefaultProfile</span></span>
<span data-ttu-id="42897-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42897-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42897-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="42897-124">-EndIPAddress</span></span>
<span data-ttu-id="42897-125">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="42897-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="42897-126">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="42897-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="42897-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42897-127">-InputObject</span></span>
<span data-ttu-id="42897-128">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="42897-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42897-129">-Name</span><span class="sxs-lookup"><span data-stu-id="42897-129">-Name</span></span>
<span data-ttu-id="42897-130">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="42897-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="42897-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="42897-131">-NoWait</span></span>
<span data-ttu-id="42897-132">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="42897-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="42897-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42897-133">-ResourceGroupName</span></span>
<span data-ttu-id="42897-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42897-134">The name of the resource group.</span></span>
<span data-ttu-id="42897-135">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="42897-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="42897-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42897-136">-ServerName</span></span>
<span data-ttu-id="42897-137">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="42897-137">The name of the server.</span></span>

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

### <span data-ttu-id="42897-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="42897-138">-StartIPAddress</span></span>
<span data-ttu-id="42897-139">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="42897-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="42897-140">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="42897-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="42897-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42897-141">-SubscriptionId</span></span>
<span data-ttu-id="42897-142">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="42897-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="42897-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42897-143">-Confirm</span></span>
<span data-ttu-id="42897-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42897-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42897-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42897-145">-WhatIf</span></span>
<span data-ttu-id="42897-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42897-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42897-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42897-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42897-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42897-148">CommonParameters</span></span>
<span data-ttu-id="42897-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42897-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42897-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42897-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42897-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="42897-151">INPUTS</span></span>

### <span data-ttu-id="42897-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="42897-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="42897-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42897-153">OUTPUTS</span></span>

### <span data-ttu-id="42897-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="42897-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="42897-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="42897-155">NOTES</span></span>

<span data-ttu-id="42897-156">ALIAS</span><span class="sxs-lookup"><span data-stu-id="42897-156">ALIASES</span></span>

<span data-ttu-id="42897-157">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="42897-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42897-158">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="42897-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42897-159">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="42897-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42897-160">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="42897-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="42897-161">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="42897-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="42897-162">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="42897-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="42897-163">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="42897-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="42897-164">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="42897-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="42897-165">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="42897-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="42897-166">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42897-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="42897-167">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="42897-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="42897-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="42897-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="42897-169">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="42897-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="42897-170">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="42897-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="42897-171">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="42897-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="42897-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42897-172">RELATED LINKS</span></span>

