---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207091"
---
# <span data-ttu-id="2aed2-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="2aed2-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="2aed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aed2-102">SYNOPSIS</span></span>
<span data-ttu-id="2aed2-103">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="2aed2-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2aed2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aed2-104">SYNTAX</span></span>

### <span data-ttu-id="2aed2-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2aed2-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2aed2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2aed2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2aed2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2aed2-107">DESCRIPTION</span></span>
<span data-ttu-id="2aed2-108">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="2aed2-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2aed2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aed2-109">EXAMPLES</span></span>

### <span data-ttu-id="2aed2-110">Esempio 1: Aggiornare un database del server MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="2aed2-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="2aed2-111">Aggiornare un database in base al nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2aed2-111">Update a database by resource name.</span></span>

### <span data-ttu-id="2aed2-112">Esempio 2: Aggiornare il database MySql in base al parametro.</span><span class="sxs-lookup"><span data-stu-id="2aed2-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="2aed2-113">Aggiornare un database in base al parametro</span><span class="sxs-lookup"><span data-stu-id="2aed2-113">Update a database by parameter</span></span>

## <span data-ttu-id="2aed2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aed2-114">PARAMETERS</span></span>

### <span data-ttu-id="2aed2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aed2-115">-AsJob</span></span>
<span data-ttu-id="2aed2-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2aed2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2aed2-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="2aed2-117">-Charset</span></span>
<span data-ttu-id="2aed2-118">Il charset del database.</span><span class="sxs-lookup"><span data-stu-id="2aed2-118">The charset of the database.</span></span>

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

### <span data-ttu-id="2aed2-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="2aed2-119">-Collation</span></span>
<span data-ttu-id="2aed2-120">Fascicolazione del database.</span><span class="sxs-lookup"><span data-stu-id="2aed2-120">The collation of the database.</span></span>

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

### <span data-ttu-id="2aed2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aed2-121">-DefaultProfile</span></span>
<span data-ttu-id="2aed2-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2aed2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aed2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aed2-123">-InputObject</span></span>
<span data-ttu-id="2aed2-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2aed2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2aed2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2aed2-125">-Name</span></span>
<span data-ttu-id="2aed2-126">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="2aed2-126">The name of the database.</span></span>

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

### <span data-ttu-id="2aed2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2aed2-127">-NoWait</span></span>
<span data-ttu-id="2aed2-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2aed2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2aed2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aed2-129">-ResourceGroupName</span></span>
<span data-ttu-id="2aed2-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2aed2-130">The name of the resource group.</span></span>
<span data-ttu-id="2aed2-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2aed2-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2aed2-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2aed2-132">-ServerName</span></span>
<span data-ttu-id="2aed2-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="2aed2-133">The name of the server.</span></span>

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

### <span data-ttu-id="2aed2-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2aed2-134">-SubscriptionId</span></span>
<span data-ttu-id="2aed2-135">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2aed2-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2aed2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aed2-136">-Confirm</span></span>
<span data-ttu-id="2aed2-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aed2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aed2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aed2-138">-WhatIf</span></span>
<span data-ttu-id="2aed2-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aed2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aed2-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aed2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aed2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aed2-141">CommonParameters</span></span>
<span data-ttu-id="2aed2-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aed2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aed2-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2aed2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aed2-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="2aed2-144">INPUTS</span></span>

### <span data-ttu-id="2aed2-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2aed2-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2aed2-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aed2-146">OUTPUTS</span></span>

### <span data-ttu-id="2aed2-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="2aed2-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="2aed2-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="2aed2-148">NOTES</span></span>

<span data-ttu-id="2aed2-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2aed2-149">ALIASES</span></span>

<span data-ttu-id="2aed2-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2aed2-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2aed2-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2aed2-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2aed2-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2aed2-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2aed2-153">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="2aed2-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2aed2-154">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="2aed2-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2aed2-155">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="2aed2-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2aed2-156">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="2aed2-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2aed2-157">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2aed2-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2aed2-158">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="2aed2-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2aed2-159">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="2aed2-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2aed2-160">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2aed2-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2aed2-161">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2aed2-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="2aed2-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2aed2-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2aed2-163">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="2aed2-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2aed2-164">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2aed2-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2aed2-165">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aed2-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2aed2-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aed2-166">RELATED LINKS</span></span>

