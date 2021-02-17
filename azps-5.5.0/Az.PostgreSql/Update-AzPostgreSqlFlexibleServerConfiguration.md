---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 82945caa08fb102c0ef5a05e95586f9c66d3d4a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183990"
---
# <span data-ttu-id="1697c-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1697c-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="1697c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1697c-102">SYNOPSIS</span></span>
<span data-ttu-id="1697c-103">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="1697c-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="1697c-104">Usare Update-AzPostgreSqlFlexibleServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="1697c-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="1697c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1697c-105">SYNTAX</span></span>

### <span data-ttu-id="1697c-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1697c-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1697c-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1697c-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1697c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1697c-108">DESCRIPTION</span></span>
<span data-ttu-id="1697c-109">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="1697c-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="1697c-110">Usare Update-AzPostgreSqlFlexibleServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="1697c-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="1697c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1697c-111">EXAMPLES</span></span>

### <span data-ttu-id="1697c-112">Esempio 1: Updatae specificata configurazione PostgreSql in base al nome</span><span class="sxs-lookup"><span data-stu-id="1697c-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="1697c-113">Questo cmdlet aggiorna la configurazione PostgreSql specificata in base al nome.</span><span class="sxs-lookup"><span data-stu-id="1697c-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="1697c-114">Esempio 1: Updatae specificato configurazione PostgreSql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="1697c-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="1697c-115">Questo cmdlet aggiorna la configurazione PostgreSql specificata in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="1697c-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="1697c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1697c-116">PARAMETERS</span></span>

### <span data-ttu-id="1697c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1697c-117">-AsJob</span></span>
<span data-ttu-id="1697c-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1697c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1697c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1697c-119">-DefaultProfile</span></span>
<span data-ttu-id="1697c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1697c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1697c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1697c-121">-InputObject</span></span>
<span data-ttu-id="1697c-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1697c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1697c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1697c-123">-Name</span></span>
<span data-ttu-id="1697c-124">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="1697c-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="1697c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1697c-125">-NoWait</span></span>
<span data-ttu-id="1697c-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1697c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1697c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1697c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1697c-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1697c-128">The name of the resource group.</span></span>
<span data-ttu-id="1697c-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1697c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1697c-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1697c-130">-ServerName</span></span>
<span data-ttu-id="1697c-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="1697c-131">The name of the server.</span></span>

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

### <span data-ttu-id="1697c-132">-Source</span><span class="sxs-lookup"><span data-stu-id="1697c-132">-Source</span></span>
<span data-ttu-id="1697c-133">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="1697c-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="1697c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1697c-134">-SubscriptionId</span></span>
<span data-ttu-id="1697c-135">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1697c-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1697c-136">-Value</span><span class="sxs-lookup"><span data-stu-id="1697c-136">-Value</span></span>
<span data-ttu-id="1697c-137">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="1697c-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="1697c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1697c-138">-Confirm</span></span>
<span data-ttu-id="1697c-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1697c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1697c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1697c-140">-WhatIf</span></span>
<span data-ttu-id="1697c-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1697c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1697c-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1697c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1697c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1697c-143">CommonParameters</span></span>
<span data-ttu-id="1697c-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1697c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1697c-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1697c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1697c-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="1697c-146">INPUTS</span></span>

### <span data-ttu-id="1697c-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1697c-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1697c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1697c-148">OUTPUTS</span></span>

### <span data-ttu-id="1697c-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="1697c-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="1697c-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="1697c-150">NOTES</span></span>

<span data-ttu-id="1697c-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1697c-151">ALIASES</span></span>

<span data-ttu-id="1697c-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1697c-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1697c-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1697c-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1697c-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1697c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1697c-155">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="1697c-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1697c-156">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="1697c-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1697c-157">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="1697c-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1697c-158">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="1697c-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1697c-159">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="1697c-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1697c-160">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="1697c-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1697c-161">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1697c-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1697c-162">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1697c-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="1697c-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1697c-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1697c-164">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="1697c-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1697c-165">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1697c-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1697c-166">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1697c-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1697c-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1697c-167">RELATED LINKS</span></span>

