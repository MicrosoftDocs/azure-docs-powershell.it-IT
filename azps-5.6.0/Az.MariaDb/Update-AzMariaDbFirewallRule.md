---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 850b1cfae70abb3e1225f9ff7bcda937dc0f0db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003885"
---
# <span data-ttu-id="b7f35-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b7f35-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="b7f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f35-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f35-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="b7f35-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b7f35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7f35-104">SYNTAX</span></span>

### <span data-ttu-id="b7f35-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7f35-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7f35-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7f35-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7f35-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7f35-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7f35-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b7f35-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7f35-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7f35-109">DESCRIPTION</span></span>
<span data-ttu-id="b7f35-110">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="b7f35-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b7f35-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7f35-111">EXAMPLES</span></span>

### <span data-ttu-id="b7f35-112">Esempio 1: Aggiornare la regola del firewall MariaDB</span><span class="sxs-lookup"><span data-stu-id="b7f35-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="b7f35-113">Questo comando aggiorna una regola del firewall MariaDB.</span><span class="sxs-lookup"><span data-stu-id="b7f35-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="b7f35-114">Esempio 2: Aggiornare la regola del firewall MariaDB in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="b7f35-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b7f35-115">Il cmdlet aggiorna la regola del firewall MariaDB in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="b7f35-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="b7f35-116">Esempio 3: Aggiornare la regola del firewall MariaDB per -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b7f35-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="b7f35-117">Il cmdlet aggiorna la regola del firewall MariaDB per -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b7f35-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="b7f35-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7f35-118">PARAMETERS</span></span>

### <span data-ttu-id="b7f35-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7f35-119">-AsJob</span></span>
<span data-ttu-id="b7f35-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b7f35-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b7f35-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7f35-121">-ClientIPAddress</span></span>
<span data-ttu-id="b7f35-122">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b7f35-123">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b7f35-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b7f35-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f35-124">-DefaultProfile</span></span>
<span data-ttu-id="b7f35-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f35-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f35-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7f35-126">-EndIPAddress</span></span>
<span data-ttu-id="b7f35-127">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b7f35-128">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b7f35-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b7f35-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7f35-129">-InputObject</span></span>
<span data-ttu-id="b7f35-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b7f35-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7f35-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b7f35-131">-Name</span></span>
<span data-ttu-id="b7f35-132">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b7f35-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b7f35-133">-NoWait</span></span>
<span data-ttu-id="b7f35-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b7f35-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b7f35-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f35-135">-ResourceGroupName</span></span>
<span data-ttu-id="b7f35-136">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b7f35-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b7f35-137">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b7f35-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b7f35-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7f35-138">-ServerName</span></span>
<span data-ttu-id="b7f35-139">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-139">The name of the server.</span></span>

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

### <span data-ttu-id="b7f35-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b7f35-140">-StartIPAddress</span></span>
<span data-ttu-id="b7f35-141">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b7f35-142">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b7f35-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b7f35-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7f35-143">-SubscriptionId</span></span>
<span data-ttu-id="b7f35-144">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f35-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b7f35-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7f35-145">-Confirm</span></span>
<span data-ttu-id="b7f35-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f35-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f35-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f35-147">-WhatIf</span></span>
<span data-ttu-id="b7f35-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7f35-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f35-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7f35-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f35-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f35-150">CommonParameters</span></span>
<span data-ttu-id="b7f35-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f35-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f35-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7f35-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f35-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7f35-153">INPUTS</span></span>

### <span data-ttu-id="b7f35-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="b7f35-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b7f35-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7f35-155">OUTPUTS</span></span>

### <span data-ttu-id="b7f35-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b7f35-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="b7f35-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7f35-157">NOTES</span></span>

<span data-ttu-id="b7f35-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b7f35-158">ALIASES</span></span>

<span data-ttu-id="b7f35-159">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b7f35-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7f35-160">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b7f35-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7f35-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7f35-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7f35-162">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b7f35-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7f35-163">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b7f35-164">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="b7f35-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b7f35-165">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b7f35-166">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b7f35-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7f35-167">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b7f35-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b7f35-168">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b7f35-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b7f35-169">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b7f35-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b7f35-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b7f35-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b7f35-171">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="b7f35-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b7f35-172">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f35-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b7f35-173">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7f35-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b7f35-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7f35-174">RELATED LINKS</span></span>

