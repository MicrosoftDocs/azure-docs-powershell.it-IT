---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179078"
---
# <span data-ttu-id="b60bf-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b60bf-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="b60bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60bf-102">SYNOPSIS</span></span>
<span data-ttu-id="b60bf-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="b60bf-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b60bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b60bf-104">SYNTAX</span></span>

### <span data-ttu-id="b60bf-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b60bf-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b60bf-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b60bf-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b60bf-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b60bf-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b60bf-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b60bf-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b60bf-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b60bf-109">DESCRIPTION</span></span>
<span data-ttu-id="b60bf-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="b60bf-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b60bf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b60bf-111">EXAMPLES</span></span>

### <span data-ttu-id="b60bf-112">Esempio 1: Aggiornare la regola del firewall PostgreSql in base al nome</span><span class="sxs-lookup"><span data-stu-id="b60bf-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b60bf-113">Questo cmdlet aggiorna la regola del firewall PostgreSql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b60bf-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="b60bf-114">Esempio 2: Aggiornare la regola del firewall PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="b60bf-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b60bf-115">Questi cmdlet aggiornano la regola del firewall PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="b60bf-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="b60bf-116">Esempio 3: Aggiornare la regola del firewall PostgreSql per -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b60bf-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="b60bf-117">Questi cmdlet aggiornano la regola del firewall PostgreSql per -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b60bf-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="b60bf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b60bf-118">PARAMETERS</span></span>

### <span data-ttu-id="b60bf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b60bf-119">-AsJob</span></span>
<span data-ttu-id="b60bf-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b60bf-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b60bf-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b60bf-121">-ClientIPAddress</span></span>
<span data-ttu-id="b60bf-122">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b60bf-123">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b60bf-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b60bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60bf-124">-DefaultProfile</span></span>
<span data-ttu-id="b60bf-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b60bf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60bf-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b60bf-126">-EndIPAddress</span></span>
<span data-ttu-id="b60bf-127">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b60bf-128">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b60bf-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b60bf-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b60bf-129">-InputObject</span></span>
<span data-ttu-id="b60bf-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b60bf-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b60bf-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b60bf-131">-Name</span></span>
<span data-ttu-id="b60bf-132">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b60bf-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b60bf-133">-NoWait</span></span>
<span data-ttu-id="b60bf-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b60bf-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b60bf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60bf-135">-ResourceGroupName</span></span>
<span data-ttu-id="b60bf-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b60bf-136">The name of the resource group.</span></span>
<span data-ttu-id="b60bf-137">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b60bf-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b60bf-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b60bf-138">-ServerName</span></span>
<span data-ttu-id="b60bf-139">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-139">The name of the server.</span></span>

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

### <span data-ttu-id="b60bf-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b60bf-140">-StartIPAddress</span></span>
<span data-ttu-id="b60bf-141">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b60bf-142">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b60bf-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b60bf-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b60bf-143">-SubscriptionId</span></span>
<span data-ttu-id="b60bf-144">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b60bf-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b60bf-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b60bf-145">-Confirm</span></span>
<span data-ttu-id="b60bf-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60bf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60bf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60bf-147">-WhatIf</span></span>
<span data-ttu-id="b60bf-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b60bf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60bf-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b60bf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60bf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60bf-150">CommonParameters</span></span>
<span data-ttu-id="b60bf-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60bf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60bf-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b60bf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60bf-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="b60bf-153">INPUTS</span></span>

### <span data-ttu-id="b60bf-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b60bf-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b60bf-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b60bf-155">OUTPUTS</span></span>

### <span data-ttu-id="b60bf-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b60bf-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b60bf-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="b60bf-157">NOTES</span></span>

<span data-ttu-id="b60bf-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b60bf-158">ALIASES</span></span>

<span data-ttu-id="b60bf-159">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b60bf-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b60bf-160">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b60bf-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b60bf-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b60bf-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b60bf-162">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b60bf-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b60bf-163">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b60bf-164">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="b60bf-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b60bf-165">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b60bf-166">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b60bf-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b60bf-167">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b60bf-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b60bf-168">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b60bf-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b60bf-169">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b60bf-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="b60bf-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b60bf-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b60bf-171">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="b60bf-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b60bf-172">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b60bf-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b60bf-173">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b60bf-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b60bf-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b60bf-174">RELATED LINKS</span></span>

