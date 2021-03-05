---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 6f1af89c1557739e218506d441e6acb109fcf773
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979805"
---
# <span data-ttu-id="9bf11-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="9bf11-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="9bf11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf11-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf11-103">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="9bf11-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="9bf11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bf11-104">SYNTAX</span></span>

### <span data-ttu-id="9bf11-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bf11-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9bf11-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9bf11-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9bf11-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9bf11-107">DESCRIPTION</span></span>
<span data-ttu-id="9bf11-108">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="9bf11-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="9bf11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bf11-109">EXAMPLES</span></span>

### <span data-ttu-id="9bf11-110">Esempio 1: Creare un nuovo database del server MySql</span><span class="sxs-lookup"><span data-stu-id="9bf11-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="9bf11-111">Creare un database con impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="9bf11-111">Create a database with default settings.</span></span>

## <span data-ttu-id="9bf11-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bf11-112">PARAMETERS</span></span>

### <span data-ttu-id="9bf11-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf11-113">-AsJob</span></span>
<span data-ttu-id="9bf11-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="9bf11-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9bf11-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="9bf11-115">-Charset</span></span>
<span data-ttu-id="9bf11-116">Il charset del database.</span><span class="sxs-lookup"><span data-stu-id="9bf11-116">The charset of the database.</span></span>

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

### <span data-ttu-id="9bf11-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="9bf11-117">-Collation</span></span>
<span data-ttu-id="9bf11-118">Fascicolazione del database.</span><span class="sxs-lookup"><span data-stu-id="9bf11-118">The collation of the database.</span></span>

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

### <span data-ttu-id="9bf11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf11-119">-DefaultProfile</span></span>
<span data-ttu-id="9bf11-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf11-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bf11-121">-InputObject</span></span>
<span data-ttu-id="9bf11-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9bf11-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf11-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9bf11-123">-Name</span></span>
<span data-ttu-id="9bf11-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="9bf11-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf11-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9bf11-125">-NoWait</span></span>
<span data-ttu-id="9bf11-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="9bf11-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9bf11-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf11-127">-ResourceGroupName</span></span>
<span data-ttu-id="9bf11-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9bf11-128">The name of the resource group.</span></span>
<span data-ttu-id="9bf11-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9bf11-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf11-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9bf11-130">-ServerName</span></span>
<span data-ttu-id="9bf11-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9bf11-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf11-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bf11-132">-SubscriptionId</span></span>
<span data-ttu-id="9bf11-133">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bf11-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf11-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bf11-134">-Confirm</span></span>
<span data-ttu-id="9bf11-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf11-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf11-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf11-136">-WhatIf</span></span>
<span data-ttu-id="9bf11-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bf11-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf11-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bf11-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf11-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf11-139">CommonParameters</span></span>
<span data-ttu-id="9bf11-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf11-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf11-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9bf11-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf11-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="9bf11-142">INPUTS</span></span>

### <span data-ttu-id="9bf11-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9bf11-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9bf11-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bf11-144">OUTPUTS</span></span>

### <span data-ttu-id="9bf11-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="9bf11-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="9bf11-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="9bf11-146">NOTES</span></span>

<span data-ttu-id="9bf11-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9bf11-147">ALIASES</span></span>

<span data-ttu-id="9bf11-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9bf11-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9bf11-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9bf11-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9bf11-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9bf11-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9bf11-151">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9bf11-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9bf11-152">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="9bf11-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9bf11-153">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="9bf11-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9bf11-154">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9bf11-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9bf11-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="9bf11-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9bf11-156">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="9bf11-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9bf11-157">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="9bf11-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9bf11-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9bf11-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9bf11-159">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9bf11-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="9bf11-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9bf11-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9bf11-161">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="9bf11-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9bf11-162">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bf11-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9bf11-163">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9bf11-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9bf11-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bf11-164">RELATED LINKS</span></span>

