---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475171"
---
# <span data-ttu-id="11679-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="11679-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="11679-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11679-102">SYNOPSIS</span></span>
<span data-ttu-id="11679-103">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="11679-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="11679-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11679-104">SYNTAX</span></span>

### <span data-ttu-id="11679-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11679-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="11679-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="11679-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11679-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11679-107">DESCRIPTION</span></span>
<span data-ttu-id="11679-108">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="11679-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="11679-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11679-109">EXAMPLES</span></span>

### <span data-ttu-id="11679-110">Esempio 1: aggiornare un database del server MySql per nome</span><span class="sxs-lookup"><span data-stu-id="11679-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="11679-111">Aggiornare un database per nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="11679-111">Update a database by resource name.</span></span>

### <span data-ttu-id="11679-112">Esempio 2: aggiornare il database MySql tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="11679-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="11679-113">Aggiornare un database per parametro</span><span class="sxs-lookup"><span data-stu-id="11679-113">Update a database by parameter</span></span>

## <span data-ttu-id="11679-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11679-114">PARAMETERS</span></span>

### <span data-ttu-id="11679-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11679-115">-AsJob</span></span>
<span data-ttu-id="11679-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="11679-116">Run the command as a job</span></span>

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

### <span data-ttu-id="11679-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="11679-117">-Charset</span></span>
<span data-ttu-id="11679-118">Il set di caratteri del database.</span><span class="sxs-lookup"><span data-stu-id="11679-118">The charset of the database.</span></span>

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

### <span data-ttu-id="11679-119">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="11679-119">-Collation</span></span>
<span data-ttu-id="11679-120">Regole di confronto del database.</span><span class="sxs-lookup"><span data-stu-id="11679-120">The collation of the database.</span></span>

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

### <span data-ttu-id="11679-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11679-121">-DefaultProfile</span></span>
<span data-ttu-id="11679-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11679-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11679-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11679-123">-InputObject</span></span>
<span data-ttu-id="11679-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="11679-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11679-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="11679-125">-Name</span></span>
<span data-ttu-id="11679-126">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="11679-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11679-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="11679-127">-NoWait</span></span>
<span data-ttu-id="11679-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="11679-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11679-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11679-129">-ResourceGroupName</span></span>
<span data-ttu-id="11679-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11679-130">The name of the resource group.</span></span>
<span data-ttu-id="11679-131">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="11679-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="11679-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="11679-132">-ServerName</span></span>
<span data-ttu-id="11679-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="11679-133">The name of the server.</span></span>

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

### <span data-ttu-id="11679-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11679-134">-SubscriptionId</span></span>
<span data-ttu-id="11679-135">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="11679-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="11679-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11679-136">-Confirm</span></span>
<span data-ttu-id="11679-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11679-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11679-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11679-138">-WhatIf</span></span>
<span data-ttu-id="11679-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11679-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11679-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11679-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11679-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11679-141">CommonParameters</span></span>
<span data-ttu-id="11679-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11679-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11679-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11679-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11679-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11679-144">INPUTS</span></span>

### <span data-ttu-id="11679-145">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="11679-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="11679-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11679-146">OUTPUTS</span></span>

### <span data-ttu-id="11679-147">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="11679-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="11679-148">Note</span><span class="sxs-lookup"><span data-stu-id="11679-148">NOTES</span></span>

<span data-ttu-id="11679-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="11679-149">ALIASES</span></span>

<span data-ttu-id="11679-150">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11679-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11679-151">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="11679-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11679-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11679-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11679-153">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="11679-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11679-154">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="11679-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="11679-155">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="11679-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="11679-156">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="11679-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="11679-157">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="11679-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11679-158">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="11679-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="11679-159">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="11679-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="11679-160">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11679-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="11679-161">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="11679-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="11679-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="11679-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="11679-163">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="11679-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="11679-164">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="11679-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="11679-165">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="11679-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="11679-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11679-166">RELATED LINKS</span></span>

