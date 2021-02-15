---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203678"
---
# <span data-ttu-id="67d15-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67d15-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="67d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d15-102">SYNOPSIS</span></span>
<span data-ttu-id="67d15-103">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="67d15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67d15-104">SYNTAX</span></span>

### <span data-ttu-id="67d15-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67d15-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="67d15-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67d15-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67d15-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67d15-107">DESCRIPTION</span></span>
<span data-ttu-id="67d15-108">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="67d15-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67d15-109">EXAMPLES</span></span>

### <span data-ttu-id="67d15-110">Esempio 1: Rimuovere una regola del firewall in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="67d15-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="67d15-111">Questo comando rimuove una regola del firewall in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="67d15-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="67d15-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d15-112">PARAMETERS</span></span>

### <span data-ttu-id="67d15-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d15-113">-AsJob</span></span>
<span data-ttu-id="67d15-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="67d15-114">Run the command as a job</span></span>

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

### <span data-ttu-id="67d15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d15-115">-DefaultProfile</span></span>
<span data-ttu-id="67d15-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67d15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d15-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67d15-117">-InputObject</span></span>
<span data-ttu-id="67d15-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="67d15-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67d15-119">-Name</span><span class="sxs-lookup"><span data-stu-id="67d15-119">-Name</span></span>
<span data-ttu-id="67d15-120">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d15-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="67d15-121">-NoWait</span></span>
<span data-ttu-id="67d15-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="67d15-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="67d15-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67d15-123">-PassThru</span></span>
<span data-ttu-id="67d15-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="67d15-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="67d15-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d15-125">-ResourceGroupName</span></span>
<span data-ttu-id="67d15-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="67d15-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="67d15-127">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="67d15-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d15-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67d15-128">-ServerName</span></span>
<span data-ttu-id="67d15-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d15-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67d15-130">-SubscriptionId</span></span>
<span data-ttu-id="67d15-131">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67d15-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d15-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d15-132">-Confirm</span></span>
<span data-ttu-id="67d15-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d15-134">-WhatIf</span></span>
<span data-ttu-id="67d15-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d15-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d15-137">CommonParameters</span></span>
<span data-ttu-id="67d15-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d15-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67d15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d15-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="67d15-140">INPUTS</span></span>

### <span data-ttu-id="67d15-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="67d15-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="67d15-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67d15-142">OUTPUTS</span></span>

### <span data-ttu-id="67d15-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67d15-143">System.Boolean</span></span>

## <span data-ttu-id="67d15-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="67d15-144">NOTES</span></span>

<span data-ttu-id="67d15-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="67d15-145">ALIASES</span></span>

<span data-ttu-id="67d15-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="67d15-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67d15-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="67d15-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67d15-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67d15-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67d15-149">INPUTOBJECT <IMariaDbIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="67d15-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67d15-150">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="67d15-151">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="67d15-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="67d15-152">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="67d15-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="67d15-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67d15-154">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="67d15-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="67d15-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="67d15-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="67d15-156">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="67d15-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="67d15-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="67d15-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="67d15-158">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="67d15-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="67d15-159">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67d15-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="67d15-160">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="67d15-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="67d15-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67d15-161">RELATED LINKS</span></span>

