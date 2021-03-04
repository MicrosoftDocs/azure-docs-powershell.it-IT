---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: c0af624683e3d12cc1b12c057caa419c5633d45f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953533"
---
# <span data-ttu-id="1c4fc-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4fc-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="1c4fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4fc-103">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="1c4fc-104">Usare Update-AzPostgreSqlServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="1c4fc-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c4fc-105">SYNTAX</span></span>

### <span data-ttu-id="1c4fc-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c4fc-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c4fc-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1c4fc-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c4fc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c4fc-108">DESCRIPTION</span></span>
<span data-ttu-id="1c4fc-109">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="1c4fc-110">Usare Update-AzPostgreSqlServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="1c4fc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c4fc-111">EXAMPLES</span></span>

### <span data-ttu-id="1c4fc-112">Esempio 1: Aggiornare la configurazione PostgreSql in base al nome</span><span class="sxs-lookup"><span data-stu-id="1c4fc-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="1c4fc-113">Questo cmdlet aggiorna la configurazione PostgreSql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="1c4fc-114">Esempio 2: Aggiornare la configurazione PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="1c4fc-115">Questi cmdlet aggiornano la configurazione PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="1c4fc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c4fc-116">PARAMETERS</span></span>

### <span data-ttu-id="1c4fc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c4fc-117">-AsJob</span></span>
<span data-ttu-id="1c4fc-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1c4fc-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1c4fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4fc-119">-DefaultProfile</span></span>
<span data-ttu-id="1c4fc-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4fc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c4fc-121">-InputObject</span></span>
<span data-ttu-id="1c4fc-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c4fc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1c4fc-123">-Name</span></span>
<span data-ttu-id="1c4fc-124">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="1c4fc-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1c4fc-125">-NoWait</span></span>
<span data-ttu-id="1c4fc-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1c4fc-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c4fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c4fc-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-128">The name of the resource group.</span></span>
<span data-ttu-id="1c4fc-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c4fc-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c4fc-130">-ServerName</span></span>
<span data-ttu-id="1c4fc-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-131">The name of the server.</span></span>

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

### <span data-ttu-id="1c4fc-132">-Source</span><span class="sxs-lookup"><span data-stu-id="1c4fc-132">-Source</span></span>
<span data-ttu-id="1c4fc-133">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="1c4fc-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c4fc-134">-SubscriptionId</span></span>
<span data-ttu-id="1c4fc-135">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1c4fc-136">-Value</span><span class="sxs-lookup"><span data-stu-id="1c4fc-136">-Value</span></span>
<span data-ttu-id="1c4fc-137">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="1c4fc-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c4fc-138">-Confirm</span></span>
<span data-ttu-id="1c4fc-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c4fc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c4fc-140">-WhatIf</span></span>
<span data-ttu-id="1c4fc-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c4fc-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c4fc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4fc-143">CommonParameters</span></span>
<span data-ttu-id="1c4fc-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4fc-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4fc-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c4fc-146">INPUTS</span></span>

### <span data-ttu-id="1c4fc-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1c4fc-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1c4fc-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c4fc-148">OUTPUTS</span></span>

### <span data-ttu-id="1c4fc-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4fc-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="1c4fc-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c4fc-150">NOTES</span></span>

<span data-ttu-id="1c4fc-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c4fc-151">ALIASES</span></span>

<span data-ttu-id="1c4fc-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1c4fc-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c4fc-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c4fc-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c4fc-155">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="1c4fc-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c4fc-156">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1c4fc-157">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1c4fc-158">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1c4fc-159">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="1c4fc-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c4fc-160">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1c4fc-161">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1c4fc-162">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="1c4fc-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1c4fc-164">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1c4fc-165">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1c4fc-166">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1c4fc-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c4fc-167">RELATED LINKS</span></span>

