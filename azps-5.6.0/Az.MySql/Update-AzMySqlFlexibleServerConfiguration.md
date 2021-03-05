---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968782"
---
# <span data-ttu-id="a080c-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a080c-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a080c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a080c-102">SYNOPSIS</span></span>
<span data-ttu-id="a080c-103">Aggiorna le informazioni su una configurazione di un server flessibile MySQL.</span><span class="sxs-lookup"><span data-stu-id="a080c-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="a080c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a080c-104">SYNTAX</span></span>

### <span data-ttu-id="a080c-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a080c-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a080c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a080c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a080c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a080c-107">DESCRIPTION</span></span>
<span data-ttu-id="a080c-108">Aggiorna le informazioni su una configurazione di un server flessibile MySQL.</span><span class="sxs-lookup"><span data-stu-id="a080c-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="a080c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a080c-109">EXAMPLES</span></span>

### <span data-ttu-id="a080c-110">Esempio 1: Aggiornare la configurazione MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="a080c-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="a080c-111">Questo cmdlet aggiorna la configurazione mySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a080c-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="a080c-112">Esempio 2: Aggiornare la configurazione di MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="a080c-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="a080c-113">Questi cmdlet aggiornano la configurazione di MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="a080c-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="a080c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a080c-114">PARAMETERS</span></span>

### <span data-ttu-id="a080c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a080c-115">-AsJob</span></span>
<span data-ttu-id="a080c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a080c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a080c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a080c-117">-DefaultProfile</span></span>
<span data-ttu-id="a080c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a080c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a080c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a080c-119">-InputObject</span></span>
<span data-ttu-id="a080c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a080c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a080c-121">-Name</span></span>
<span data-ttu-id="a080c-122">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="a080c-122">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a080c-123">-NoWait</span></span>
<span data-ttu-id="a080c-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a080c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a080c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a080c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a080c-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a080c-126">The name of the resource group.</span></span>
<span data-ttu-id="a080c-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a080c-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a080c-128">-ServerName</span></span>
<span data-ttu-id="a080c-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="a080c-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-130">-Source</span><span class="sxs-lookup"><span data-stu-id="a080c-130">-Source</span></span>
<span data-ttu-id="a080c-131">Origine del valore aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a080c-131">The source of the updating value.</span></span>
<span data-ttu-id="a080c-132">Il valore predefinito è user-override</span><span class="sxs-lookup"><span data-stu-id="a080c-132">The default value is user-override</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a080c-133">-SubscriptionId</span></span>
<span data-ttu-id="a080c-134">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a080c-134">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-135">-Value</span><span class="sxs-lookup"><span data-stu-id="a080c-135">-Value</span></span>
<span data-ttu-id="a080c-136">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="a080c-136">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a080c-137">-Confirm</span></span>
<span data-ttu-id="a080c-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a080c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a080c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a080c-139">-WhatIf</span></span>
<span data-ttu-id="a080c-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a080c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a080c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a080c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a080c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a080c-142">CommonParameters</span></span>
<span data-ttu-id="a080c-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a080c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a080c-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a080c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a080c-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="a080c-145">INPUTS</span></span>

### <span data-ttu-id="a080c-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a080c-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a080c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a080c-147">OUTPUTS</span></span>

### <span data-ttu-id="a080c-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a080c-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a080c-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="a080c-149">NOTES</span></span>

<span data-ttu-id="a080c-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a080c-150">ALIASES</span></span>

<span data-ttu-id="a080c-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a080c-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a080c-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a080c-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a080c-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a080c-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a080c-154">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a080c-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a080c-155">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="a080c-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a080c-156">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="a080c-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a080c-157">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="a080c-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a080c-158">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a080c-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a080c-159">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="a080c-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a080c-160">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="a080c-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a080c-161">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a080c-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a080c-162">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a080c-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="a080c-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a080c-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a080c-164">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="a080c-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a080c-165">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a080c-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a080c-166">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a080c-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a080c-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a080c-167">RELATED LINKS</span></span>

