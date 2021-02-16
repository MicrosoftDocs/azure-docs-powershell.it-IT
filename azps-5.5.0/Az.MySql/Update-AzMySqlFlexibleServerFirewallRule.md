---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187326"
---
# <span data-ttu-id="ca1cc-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca1cc-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="ca1cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1cc-103">Aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="ca1cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca1cc-104">SYNTAX</span></span>

### <span data-ttu-id="ca1cc-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca1cc-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca1cc-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ca1cc-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca1cc-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca1cc-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca1cc-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ca1cc-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ca1cc-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca1cc-109">DESCRIPTION</span></span>
<span data-ttu-id="ca1cc-110">Aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="ca1cc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca1cc-111">EXAMPLES</span></span>

### <span data-ttu-id="ca1cc-112">Esempio 1: Aggiornare la regola del firewall MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="ca1cc-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="ca1cc-113">Questo cmdlet aggiorna la regola del firewall MySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="ca1cc-114">Esempio 2: Aggiornare la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="ca1cc-115">Questi cmdlet aggiornano la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="ca1cc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca1cc-116">PARAMETERS</span></span>

### <span data-ttu-id="ca1cc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca1cc-117">-AsJob</span></span>
<span data-ttu-id="ca1cc-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ca1cc-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ca1cc-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ca1cc-119">-ClientIPAddress</span></span>
<span data-ttu-id="ca1cc-120">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="ca1cc-121">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ca1cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1cc-122">-DefaultProfile</span></span>
<span data-ttu-id="ca1cc-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca1cc-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="ca1cc-124">-EndIPAddress</span></span>
<span data-ttu-id="ca1cc-125">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="ca1cc-126">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ca1cc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca1cc-127">-InputObject</span></span>
<span data-ttu-id="ca1cc-128">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca1cc-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ca1cc-129">-Name</span></span>
<span data-ttu-id="ca1cc-130">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="ca1cc-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca1cc-131">-NoWait</span></span>
<span data-ttu-id="ca1cc-132">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ca1cc-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca1cc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1cc-133">-ResourceGroupName</span></span>
<span data-ttu-id="ca1cc-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-134">The name of the resource group.</span></span>
<span data-ttu-id="ca1cc-135">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ca1cc-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca1cc-136">-ServerName</span></span>
<span data-ttu-id="ca1cc-137">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-137">The name of the server.</span></span>

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

### <span data-ttu-id="ca1cc-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="ca1cc-138">-StartIPAddress</span></span>
<span data-ttu-id="ca1cc-139">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="ca1cc-140">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ca1cc-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca1cc-141">-SubscriptionId</span></span>
<span data-ttu-id="ca1cc-142">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ca1cc-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca1cc-143">-Confirm</span></span>
<span data-ttu-id="ca1cc-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1cc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1cc-145">-WhatIf</span></span>
<span data-ttu-id="ca1cc-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1cc-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1cc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1cc-148">CommonParameters</span></span>
<span data-ttu-id="ca1cc-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1cc-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1cc-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca1cc-151">INPUTS</span></span>

### <span data-ttu-id="ca1cc-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ca1cc-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ca1cc-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca1cc-153">OUTPUTS</span></span>

### <span data-ttu-id="ca1cc-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca1cc-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ca1cc-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca1cc-155">NOTES</span></span>

<span data-ttu-id="ca1cc-156">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca1cc-156">ALIASES</span></span>

<span data-ttu-id="ca1cc-157">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ca1cc-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca1cc-158">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca1cc-159">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca1cc-160">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="ca1cc-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca1cc-161">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ca1cc-162">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ca1cc-163">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ca1cc-164">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="ca1cc-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca1cc-165">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ca1cc-166">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ca1cc-167">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ca1cc-168">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="ca1cc-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ca1cc-170">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ca1cc-171">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ca1cc-172">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca1cc-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ca1cc-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca1cc-173">RELATED LINKS</span></span>

