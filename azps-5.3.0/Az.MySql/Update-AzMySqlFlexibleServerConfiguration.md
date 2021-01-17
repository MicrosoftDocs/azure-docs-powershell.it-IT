---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475174"
---
# <span data-ttu-id="ac234-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac234-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="ac234-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac234-102">SYNOPSIS</span></span>
<span data-ttu-id="ac234-103">Aggiorna le informazioni relative a una configurazione di un server MySQL flexible.</span><span class="sxs-lookup"><span data-stu-id="ac234-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="ac234-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac234-104">SYNTAX</span></span>

### <span data-ttu-id="ac234-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac234-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac234-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac234-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac234-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac234-107">DESCRIPTION</span></span>
<span data-ttu-id="ac234-108">Aggiorna le informazioni relative a una configurazione di un server MySQL flexible.</span><span class="sxs-lookup"><span data-stu-id="ac234-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="ac234-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac234-109">EXAMPLES</span></span>

### <span data-ttu-id="ac234-110">Esempio 1: aggiornare la configurazione di MySql per nome</span><span class="sxs-lookup"><span data-stu-id="ac234-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="ac234-111">Questo cmdlet aggiorna la configurazione di MySql per nome.</span><span class="sxs-lookup"><span data-stu-id="ac234-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="ac234-112">Esempio 2: aggiornare la configurazione di MySql per identità.</span><span class="sxs-lookup"><span data-stu-id="ac234-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="ac234-113">Questi cmdlet aggiornano la configurazione di MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="ac234-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="ac234-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac234-114">PARAMETERS</span></span>

### <span data-ttu-id="ac234-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac234-115">-AsJob</span></span>
<span data-ttu-id="ac234-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ac234-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ac234-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac234-117">-DefaultProfile</span></span>
<span data-ttu-id="ac234-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac234-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac234-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac234-119">-InputObject</span></span>
<span data-ttu-id="ac234-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ac234-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac234-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac234-121">-Name</span></span>
<span data-ttu-id="ac234-122">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="ac234-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="ac234-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ac234-123">-NoWait</span></span>
<span data-ttu-id="ac234-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ac234-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac234-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac234-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac234-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac234-126">The name of the resource group.</span></span>
<span data-ttu-id="ac234-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ac234-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac234-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ac234-128">-ServerName</span></span>
<span data-ttu-id="ac234-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ac234-129">The name of the server.</span></span>

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

### <span data-ttu-id="ac234-130">-Origine</span><span class="sxs-lookup"><span data-stu-id="ac234-130">-Source</span></span>
<span data-ttu-id="ac234-131">L'origine del valore di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ac234-131">The source of the updating value.</span></span>
<span data-ttu-id="ac234-132">Il valore predefinito è User-override</span><span class="sxs-lookup"><span data-stu-id="ac234-132">The default value is user-override</span></span>

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

### <span data-ttu-id="ac234-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac234-133">-SubscriptionId</span></span>
<span data-ttu-id="ac234-134">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ac234-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ac234-135">-Valore</span><span class="sxs-lookup"><span data-stu-id="ac234-135">-Value</span></span>
<span data-ttu-id="ac234-136">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="ac234-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="ac234-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac234-137">-Confirm</span></span>
<span data-ttu-id="ac234-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac234-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac234-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac234-139">-WhatIf</span></span>
<span data-ttu-id="ac234-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac234-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac234-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac234-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac234-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac234-142">CommonParameters</span></span>
<span data-ttu-id="ac234-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac234-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac234-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac234-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac234-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac234-145">INPUTS</span></span>

### <span data-ttu-id="ac234-146">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ac234-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ac234-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac234-147">OUTPUTS</span></span>

### <span data-ttu-id="ac234-148">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ac234-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="ac234-149">Note</span><span class="sxs-lookup"><span data-stu-id="ac234-149">NOTES</span></span>

<span data-ttu-id="ac234-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac234-150">ALIASES</span></span>

<span data-ttu-id="ac234-151">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac234-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac234-152">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ac234-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac234-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac234-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac234-154">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ac234-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac234-155">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="ac234-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ac234-156">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ac234-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ac234-157">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ac234-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ac234-158">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ac234-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac234-159">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="ac234-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ac234-160">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="ac234-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ac234-161">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac234-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac234-162">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ac234-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac234-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ac234-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ac234-164">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ac234-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ac234-165">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ac234-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac234-166">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac234-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ac234-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac234-167">RELATED LINKS</span></span>

