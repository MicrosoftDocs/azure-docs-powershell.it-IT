---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 481761efe01646a10118d8ebfd645375caafbfef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190039"
---
# <span data-ttu-id="89baf-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89baf-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="89baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89baf-102">SYNOPSIS</span></span>
<span data-ttu-id="89baf-103">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="89baf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89baf-104">SYNTAX</span></span>

### <span data-ttu-id="89baf-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89baf-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="89baf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89baf-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89baf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="89baf-107">DESCRIPTION</span></span>
<span data-ttu-id="89baf-108">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="89baf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89baf-109">EXAMPLES</span></span>

### <span data-ttu-id="89baf-110">Esempio 1: Rimuovere la regola del firewall MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="89baf-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="89baf-111">Questo cmdlet rimuove la regola del firewall MySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="89baf-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="89baf-112">Esempio 2: Rimuovere la regola del firewall MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="89baf-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="89baf-113">Questi cmdlet rimuovono la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="89baf-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="89baf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89baf-114">PARAMETERS</span></span>

### <span data-ttu-id="89baf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89baf-115">-AsJob</span></span>
<span data-ttu-id="89baf-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="89baf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="89baf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89baf-117">-DefaultProfile</span></span>
<span data-ttu-id="89baf-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89baf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89baf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89baf-119">-InputObject</span></span>
<span data-ttu-id="89baf-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="89baf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89baf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="89baf-121">-Name</span></span>
<span data-ttu-id="89baf-122">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="89baf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89baf-123">-NoWait</span></span>
<span data-ttu-id="89baf-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="89baf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89baf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89baf-125">-PassThru</span></span>
<span data-ttu-id="89baf-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="89baf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="89baf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89baf-127">-ResourceGroupName</span></span>
<span data-ttu-id="89baf-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89baf-128">The name of the resource group.</span></span>
<span data-ttu-id="89baf-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="89baf-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="89baf-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89baf-130">-ServerName</span></span>
<span data-ttu-id="89baf-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-131">The name of the server.</span></span>

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

### <span data-ttu-id="89baf-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89baf-132">-SubscriptionId</span></span>
<span data-ttu-id="89baf-133">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89baf-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="89baf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89baf-134">-Confirm</span></span>
<span data-ttu-id="89baf-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89baf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89baf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89baf-136">-WhatIf</span></span>
<span data-ttu-id="89baf-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89baf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89baf-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89baf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89baf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89baf-139">CommonParameters</span></span>
<span data-ttu-id="89baf-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89baf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89baf-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89baf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89baf-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="89baf-142">INPUTS</span></span>

### <span data-ttu-id="89baf-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="89baf-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="89baf-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89baf-144">OUTPUTS</span></span>

### <span data-ttu-id="89baf-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89baf-145">System.Boolean</span></span>

## <span data-ttu-id="89baf-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="89baf-146">NOTES</span></span>

<span data-ttu-id="89baf-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="89baf-147">ALIASES</span></span>

<span data-ttu-id="89baf-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="89baf-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89baf-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="89baf-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89baf-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89baf-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89baf-151">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="89baf-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89baf-152">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="89baf-153">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="89baf-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="89baf-154">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="89baf-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="89baf-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89baf-156">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="89baf-157">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="89baf-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="89baf-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89baf-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="89baf-159">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="89baf-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="89baf-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="89baf-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="89baf-161">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="89baf-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="89baf-162">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89baf-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="89baf-163">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="89baf-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="89baf-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89baf-164">RELATED LINKS</span></span>

