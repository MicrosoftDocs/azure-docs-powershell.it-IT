---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380628"
---
# <span data-ttu-id="71797-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="71797-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="71797-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71797-102">SYNOPSIS</span></span>
<span data-ttu-id="71797-103">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="71797-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="71797-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71797-104">SYNTAX</span></span>

### <span data-ttu-id="71797-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71797-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71797-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="71797-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71797-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71797-107">DESCRIPTION</span></span>
<span data-ttu-id="71797-108">Crea un nuovo database o aggiorna un database esistente.</span><span class="sxs-lookup"><span data-stu-id="71797-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="71797-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71797-109">EXAMPLES</span></span>

### <span data-ttu-id="71797-110">Esempio 1: creare un nuovo database del server MySql</span><span class="sxs-lookup"><span data-stu-id="71797-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="71797-111">Creare un database con le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="71797-111">Create a database with default settings.</span></span>

## <span data-ttu-id="71797-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71797-112">PARAMETERS</span></span>

### <span data-ttu-id="71797-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71797-113">-AsJob</span></span>
<span data-ttu-id="71797-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="71797-114">Run the command as a job</span></span>

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

### <span data-ttu-id="71797-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="71797-115">-Charset</span></span>
<span data-ttu-id="71797-116">Il set di caratteri del database.</span><span class="sxs-lookup"><span data-stu-id="71797-116">The charset of the database.</span></span>

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

### <span data-ttu-id="71797-117">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="71797-117">-Collation</span></span>
<span data-ttu-id="71797-118">Regole di confronto del database.</span><span class="sxs-lookup"><span data-stu-id="71797-118">The collation of the database.</span></span>

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

### <span data-ttu-id="71797-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71797-119">-DefaultProfile</span></span>
<span data-ttu-id="71797-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71797-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71797-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71797-121">-InputObject</span></span>
<span data-ttu-id="71797-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="71797-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71797-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="71797-123">-Name</span></span>
<span data-ttu-id="71797-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="71797-124">The name of the database.</span></span>

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

### <span data-ttu-id="71797-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="71797-125">-NoWait</span></span>
<span data-ttu-id="71797-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="71797-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71797-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71797-127">-ResourceGroupName</span></span>
<span data-ttu-id="71797-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71797-128">The name of the resource group.</span></span>
<span data-ttu-id="71797-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="71797-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="71797-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="71797-130">-ServerName</span></span>
<span data-ttu-id="71797-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="71797-131">The name of the server.</span></span>

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

### <span data-ttu-id="71797-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71797-132">-SubscriptionId</span></span>
<span data-ttu-id="71797-133">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71797-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="71797-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71797-134">-Confirm</span></span>
<span data-ttu-id="71797-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71797-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71797-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71797-136">-WhatIf</span></span>
<span data-ttu-id="71797-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71797-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71797-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71797-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71797-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71797-139">CommonParameters</span></span>
<span data-ttu-id="71797-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71797-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71797-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71797-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71797-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71797-142">INPUTS</span></span>

### <span data-ttu-id="71797-143">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="71797-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="71797-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71797-144">OUTPUTS</span></span>

### <span data-ttu-id="71797-145">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="71797-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="71797-146">Note</span><span class="sxs-lookup"><span data-stu-id="71797-146">NOTES</span></span>

<span data-ttu-id="71797-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="71797-147">ALIASES</span></span>

<span data-ttu-id="71797-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71797-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71797-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="71797-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71797-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71797-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71797-151">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="71797-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71797-152">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="71797-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="71797-153">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="71797-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="71797-154">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="71797-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="71797-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="71797-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71797-156">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="71797-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="71797-157">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="71797-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="71797-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71797-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="71797-159">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="71797-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="71797-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="71797-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="71797-161">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="71797-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="71797-162">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71797-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="71797-163">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="71797-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="71797-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71797-164">RELATED LINKS</span></span>

