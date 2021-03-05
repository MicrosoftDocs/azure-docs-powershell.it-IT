---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 7d356bc977ce02d998230ad755f43479e09f0a66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968781"
---
# <span data-ttu-id="b50d5-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="b50d5-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="b50d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b50d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b50d5-103">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="b50d5-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="b50d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b50d5-104">SYNTAX</span></span>

### <span data-ttu-id="b50d5-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b50d5-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b50d5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b50d5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b50d5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b50d5-107">DESCRIPTION</span></span>
<span data-ttu-id="b50d5-108">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="b50d5-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="b50d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b50d5-109">EXAMPLES</span></span>

### <span data-ttu-id="b50d5-110">Esempio 1: Aggiornare un database del server MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="b50d5-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="b50d5-111">Aggiornare un database in base al nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b50d5-111">Update a database by resource name.</span></span>

### <span data-ttu-id="b50d5-112">Esempio 2: Aggiornare il database MySql in base al parametro.</span><span class="sxs-lookup"><span data-stu-id="b50d5-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="b50d5-113">Aggiornare un database in base al parametro</span><span class="sxs-lookup"><span data-stu-id="b50d5-113">Update a database by parameter</span></span>

## <span data-ttu-id="b50d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b50d5-114">PARAMETERS</span></span>

### <span data-ttu-id="b50d5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b50d5-115">-AsJob</span></span>
<span data-ttu-id="b50d5-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b50d5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b50d5-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="b50d5-117">-Charset</span></span>
<span data-ttu-id="b50d5-118">Il charset del database.</span><span class="sxs-lookup"><span data-stu-id="b50d5-118">The charset of the database.</span></span>

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

### <span data-ttu-id="b50d5-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="b50d5-119">-Collation</span></span>
<span data-ttu-id="b50d5-120">Fascicolazione del database.</span><span class="sxs-lookup"><span data-stu-id="b50d5-120">The collation of the database.</span></span>

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

### <span data-ttu-id="b50d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50d5-121">-DefaultProfile</span></span>
<span data-ttu-id="b50d5-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b50d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b50d5-123">-InputObject</span></span>
<span data-ttu-id="b50d5-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b50d5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b50d5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b50d5-125">-Name</span></span>
<span data-ttu-id="b50d5-126">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="b50d5-126">The name of the database.</span></span>

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

### <span data-ttu-id="b50d5-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b50d5-127">-NoWait</span></span>
<span data-ttu-id="b50d5-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b50d5-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b50d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b50d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b50d5-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b50d5-130">The name of the resource group.</span></span>
<span data-ttu-id="b50d5-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b50d5-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b50d5-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b50d5-132">-ServerName</span></span>
<span data-ttu-id="b50d5-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b50d5-133">The name of the server.</span></span>

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

### <span data-ttu-id="b50d5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b50d5-134">-SubscriptionId</span></span>
<span data-ttu-id="b50d5-135">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b50d5-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b50d5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b50d5-136">-Confirm</span></span>
<span data-ttu-id="b50d5-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b50d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b50d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50d5-138">-WhatIf</span></span>
<span data-ttu-id="b50d5-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b50d5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b50d5-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b50d5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b50d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50d5-141">CommonParameters</span></span>
<span data-ttu-id="b50d5-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50d5-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b50d5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50d5-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="b50d5-144">INPUTS</span></span>

### <span data-ttu-id="b50d5-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b50d5-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b50d5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b50d5-146">OUTPUTS</span></span>

### <span data-ttu-id="b50d5-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="b50d5-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="b50d5-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="b50d5-148">NOTES</span></span>

<span data-ttu-id="b50d5-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b50d5-149">ALIASES</span></span>

<span data-ttu-id="b50d5-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b50d5-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b50d5-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b50d5-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b50d5-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b50d5-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b50d5-153">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b50d5-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b50d5-154">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="b50d5-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b50d5-155">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="b50d5-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b50d5-156">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b50d5-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b50d5-157">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b50d5-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b50d5-158">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="b50d5-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b50d5-159">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b50d5-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b50d5-160">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b50d5-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b50d5-161">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b50d5-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="b50d5-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b50d5-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b50d5-163">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="b50d5-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b50d5-164">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b50d5-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b50d5-165">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b50d5-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b50d5-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b50d5-166">RELATED LINKS</span></span>

