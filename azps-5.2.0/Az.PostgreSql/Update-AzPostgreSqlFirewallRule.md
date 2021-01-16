---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331135"
---
# <span data-ttu-id="7cbda-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7cbda-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="7cbda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cbda-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbda-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="7cbda-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="7cbda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cbda-104">SYNTAX</span></span>

### <span data-ttu-id="7cbda-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7cbda-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cbda-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7cbda-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cbda-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7cbda-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cbda-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7cbda-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7cbda-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cbda-109">DESCRIPTION</span></span>
<span data-ttu-id="7cbda-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="7cbda-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="7cbda-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cbda-111">EXAMPLES</span></span>

### <span data-ttu-id="7cbda-112">Esempio 1: aggiornare la regola del firewall PostgreSql per nome</span><span class="sxs-lookup"><span data-stu-id="7cbda-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="7cbda-113">Questo cmdlet aggiorna la regola del firewall PostgreSql per nome.</span><span class="sxs-lookup"><span data-stu-id="7cbda-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="7cbda-114">Esempio 2: aggiornare la regola del firewall PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="7cbda-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="7cbda-115">Questi cmdlet aggiornano la regola del firewall PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="7cbda-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="7cbda-116">Esempio 3: aggiornare la regola del firewall di PostgreSql per-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="7cbda-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="7cbda-117">Questi cmdlet aggiornano la regola del firewall PostgreSql da-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="7cbda-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="7cbda-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cbda-118">PARAMETERS</span></span>

### <span data-ttu-id="7cbda-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cbda-119">-AsJob</span></span>
<span data-ttu-id="7cbda-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7cbda-120">Run the command as a job</span></span>

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

### <span data-ttu-id="7cbda-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7cbda-121">-ClientIPAddress</span></span>
<span data-ttu-id="7cbda-122">Il client ha specificato un singolo IP della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="7cbda-123">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="7cbda-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7cbda-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbda-124">-DefaultProfile</span></span>
<span data-ttu-id="7cbda-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbda-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cbda-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="7cbda-126">-EndIPAddress</span></span>
<span data-ttu-id="7cbda-127">Indirizzo IP finale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="7cbda-128">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="7cbda-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7cbda-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cbda-129">-InputObject</span></span>
<span data-ttu-id="7cbda-130">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7cbda-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7cbda-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cbda-131">-Name</span></span>
<span data-ttu-id="7cbda-132">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="7cbda-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="7cbda-133">-NoWait</span></span>
<span data-ttu-id="7cbda-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7cbda-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7cbda-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbda-135">-ResourceGroupName</span></span>
<span data-ttu-id="7cbda-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7cbda-136">The name of the resource group.</span></span>
<span data-ttu-id="7cbda-137">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7cbda-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7cbda-138">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7cbda-138">-ServerName</span></span>
<span data-ttu-id="7cbda-139">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-139">The name of the server.</span></span>

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

### <span data-ttu-id="7cbda-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="7cbda-140">-StartIPAddress</span></span>
<span data-ttu-id="7cbda-141">Indirizzo IP iniziale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="7cbda-142">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="7cbda-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7cbda-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cbda-143">-SubscriptionId</span></span>
<span data-ttu-id="7cbda-144">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7cbda-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7cbda-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7cbda-145">-Confirm</span></span>
<span data-ttu-id="7cbda-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cbda-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbda-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbda-147">-WhatIf</span></span>
<span data-ttu-id="7cbda-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cbda-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbda-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cbda-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbda-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbda-150">CommonParameters</span></span>
<span data-ttu-id="7cbda-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbda-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbda-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cbda-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbda-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cbda-153">INPUTS</span></span>

### <span data-ttu-id="7cbda-154">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7cbda-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7cbda-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cbda-155">OUTPUTS</span></span>

### <span data-ttu-id="7cbda-156">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7cbda-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="7cbda-157">Note</span><span class="sxs-lookup"><span data-stu-id="7cbda-157">NOTES</span></span>

<span data-ttu-id="7cbda-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7cbda-158">ALIASES</span></span>

<span data-ttu-id="7cbda-159">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cbda-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cbda-160">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7cbda-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cbda-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cbda-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cbda-162">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7cbda-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cbda-163">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7cbda-164">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="7cbda-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7cbda-165">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7cbda-166">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7cbda-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cbda-167">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="7cbda-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7cbda-168">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7cbda-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7cbda-169">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7cbda-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="7cbda-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cbda-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7cbda-171">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="7cbda-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7cbda-172">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7cbda-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7cbda-173">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7cbda-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7cbda-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cbda-174">RELATED LINKS</span></span>

