---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202850"
---
# <span data-ttu-id="01955-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01955-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="01955-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01955-102">SYNOPSIS</span></span>
<span data-ttu-id="01955-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="01955-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="01955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01955-104">SYNTAX</span></span>

### <span data-ttu-id="01955-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01955-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01955-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="01955-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01955-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01955-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01955-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="01955-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01955-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01955-109">DESCRIPTION</span></span>
<span data-ttu-id="01955-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="01955-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="01955-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01955-111">EXAMPLES</span></span>

### <span data-ttu-id="01955-112">Esempio 1: aggiornare la regola del firewall MySql per nome</span><span class="sxs-lookup"><span data-stu-id="01955-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="01955-113">Questo cmdlet aggiorna la regola del firewall MySql per nome.</span><span class="sxs-lookup"><span data-stu-id="01955-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="01955-114">Esempio 2: aggiornare la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="01955-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="01955-115">Questi cmdlet aggiornano la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="01955-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="01955-116">Esempio 3: aggiornare la regola del firewall di MySql da-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="01955-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="01955-117">Questi cmdlet aggiornano la regola del firewall di MySql da-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="01955-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="01955-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01955-118">PARAMETERS</span></span>

### <span data-ttu-id="01955-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01955-119">-AsJob</span></span>
<span data-ttu-id="01955-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="01955-120">Run the command as a job</span></span>

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

### <span data-ttu-id="01955-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="01955-121">-ClientIPAddress</span></span>
<span data-ttu-id="01955-122">Il client ha specificato un singolo IP della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="01955-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="01955-123">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="01955-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="01955-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01955-124">-DefaultProfile</span></span>
<span data-ttu-id="01955-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01955-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01955-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="01955-126">-EndIPAddress</span></span>
<span data-ttu-id="01955-127">Indirizzo IP finale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="01955-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="01955-128">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="01955-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="01955-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01955-129">-InputObject</span></span>
<span data-ttu-id="01955-130">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="01955-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="01955-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="01955-131">-Name</span></span>
<span data-ttu-id="01955-132">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="01955-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="01955-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="01955-133">-NoWait</span></span>
<span data-ttu-id="01955-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="01955-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01955-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01955-135">-ResourceGroupName</span></span>
<span data-ttu-id="01955-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01955-136">The name of the resource group.</span></span>
<span data-ttu-id="01955-137">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="01955-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="01955-138">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="01955-138">-ServerName</span></span>
<span data-ttu-id="01955-139">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="01955-139">The name of the server.</span></span>

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

### <span data-ttu-id="01955-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="01955-140">-StartIPAddress</span></span>
<span data-ttu-id="01955-141">Indirizzo IP iniziale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="01955-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="01955-142">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="01955-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="01955-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01955-143">-SubscriptionId</span></span>
<span data-ttu-id="01955-144">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01955-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="01955-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01955-145">-Confirm</span></span>
<span data-ttu-id="01955-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01955-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01955-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01955-147">-WhatIf</span></span>
<span data-ttu-id="01955-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01955-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01955-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01955-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01955-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01955-150">CommonParameters</span></span>
<span data-ttu-id="01955-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01955-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01955-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01955-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01955-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01955-153">INPUTS</span></span>

### <span data-ttu-id="01955-154">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="01955-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="01955-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01955-155">OUTPUTS</span></span>

### <span data-ttu-id="01955-156">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01955-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="01955-157">Note</span><span class="sxs-lookup"><span data-stu-id="01955-157">NOTES</span></span>

<span data-ttu-id="01955-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="01955-158">ALIASES</span></span>

<span data-ttu-id="01955-159">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01955-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01955-160">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="01955-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01955-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01955-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01955-162">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="01955-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01955-163">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="01955-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="01955-164">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="01955-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="01955-165">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="01955-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="01955-166">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="01955-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01955-167">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="01955-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="01955-168">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01955-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="01955-169">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="01955-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="01955-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="01955-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="01955-171">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="01955-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="01955-172">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01955-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="01955-173">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="01955-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="01955-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01955-174">RELATED LINKS</span></span>

