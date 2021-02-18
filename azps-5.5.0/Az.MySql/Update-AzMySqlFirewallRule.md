---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: eb74b9530c9ce196b308a310d5a20642328719e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207098"
---
# <span data-ttu-id="4a74a-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4a74a-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="4a74a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a74a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a74a-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="4a74a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="4a74a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a74a-104">SYNTAX</span></span>

### <span data-ttu-id="4a74a-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a74a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a74a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="4a74a-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a74a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a74a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a74a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4a74a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a74a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a74a-109">DESCRIPTION</span></span>
<span data-ttu-id="4a74a-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="4a74a-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="4a74a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a74a-111">EXAMPLES</span></span>

### <span data-ttu-id="4a74a-112">Esempio 1: Aggiornare la regola del firewall MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="4a74a-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="4a74a-113">Questo cmdlet aggiorna la regola del firewall MySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="4a74a-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="4a74a-114">Esempio 2: Aggiornare la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="4a74a-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="4a74a-115">Questi cmdlet aggiornano la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="4a74a-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="4a74a-116">Esempio 3: Aggiornare la regola del firewall MySql per -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="4a74a-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="4a74a-117">Questi cmdlet aggiornano la regola del firewall MySql per -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="4a74a-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="4a74a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a74a-118">PARAMETERS</span></span>

### <span data-ttu-id="4a74a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a74a-119">-AsJob</span></span>
<span data-ttu-id="4a74a-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4a74a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="4a74a-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="4a74a-121">-ClientIPAddress</span></span>
<span data-ttu-id="4a74a-122">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="4a74a-123">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="4a74a-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4a74a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a74a-124">-DefaultProfile</span></span>
<span data-ttu-id="4a74a-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a74a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a74a-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="4a74a-126">-EndIPAddress</span></span>
<span data-ttu-id="4a74a-127">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="4a74a-128">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="4a74a-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4a74a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a74a-129">-InputObject</span></span>
<span data-ttu-id="4a74a-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4a74a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a74a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4a74a-131">-Name</span></span>
<span data-ttu-id="4a74a-132">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="4a74a-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a74a-133">-NoWait</span></span>
<span data-ttu-id="4a74a-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4a74a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a74a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a74a-135">-ResourceGroupName</span></span>
<span data-ttu-id="4a74a-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a74a-136">The name of the resource group.</span></span>
<span data-ttu-id="4a74a-137">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a74a-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4a74a-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a74a-138">-ServerName</span></span>
<span data-ttu-id="4a74a-139">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-139">The name of the server.</span></span>

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

### <span data-ttu-id="4a74a-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="4a74a-140">-StartIPAddress</span></span>
<span data-ttu-id="4a74a-141">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="4a74a-142">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="4a74a-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4a74a-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a74a-143">-SubscriptionId</span></span>
<span data-ttu-id="4a74a-144">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a74a-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4a74a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a74a-145">-Confirm</span></span>
<span data-ttu-id="4a74a-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a74a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a74a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a74a-147">-WhatIf</span></span>
<span data-ttu-id="4a74a-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a74a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a74a-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a74a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a74a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a74a-150">CommonParameters</span></span>
<span data-ttu-id="4a74a-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a74a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a74a-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a74a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a74a-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a74a-153">INPUTS</span></span>

### <span data-ttu-id="4a74a-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4a74a-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4a74a-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a74a-155">OUTPUTS</span></span>

### <span data-ttu-id="4a74a-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4a74a-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="4a74a-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a74a-157">NOTES</span></span>

<span data-ttu-id="4a74a-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4a74a-158">ALIASES</span></span>

<span data-ttu-id="4a74a-159">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4a74a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a74a-160">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4a74a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a74a-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a74a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a74a-162">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="4a74a-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a74a-163">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4a74a-164">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="4a74a-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4a74a-165">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4a74a-166">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4a74a-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a74a-167">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-167">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4a74a-168">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="4a74a-168">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4a74a-169">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a74a-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4a74a-170">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a74a-170">The name is case insensitive.</span></span>
  - <span data-ttu-id="4a74a-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4a74a-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4a74a-172">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="4a74a-172">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4a74a-173">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a74a-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4a74a-174">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a74a-174">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4a74a-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a74a-175">RELATED LINKS</span></span>

