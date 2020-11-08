---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188307"
---
# <span data-ttu-id="6e67e-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e67e-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="6e67e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e67e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e67e-103">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="6e67e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e67e-104">SYNTAX</span></span>

### <span data-ttu-id="6e67e-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e67e-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6e67e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e67e-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e67e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e67e-107">DESCRIPTION</span></span>
<span data-ttu-id="6e67e-108">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="6e67e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e67e-109">EXAMPLES</span></span>

### <span data-ttu-id="6e67e-110">Esempio 1: rimuovere la regola del firewall PostgreSql per nome</span><span class="sxs-lookup"><span data-stu-id="6e67e-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="6e67e-111">Questo cmdlet rimuove la regola del firewall PostgreSql per nome.</span><span class="sxs-lookup"><span data-stu-id="6e67e-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="6e67e-112">Esempio 2: rimuovere la regola del firewall PostgreSql per identità</span><span class="sxs-lookup"><span data-stu-id="6e67e-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="6e67e-113">Questi cmdlet eliminano la regola del firewall PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="6e67e-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="6e67e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e67e-114">PARAMETERS</span></span>

### <span data-ttu-id="6e67e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e67e-115">-AsJob</span></span>
<span data-ttu-id="6e67e-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6e67e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6e67e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e67e-117">-DefaultProfile</span></span>
<span data-ttu-id="6e67e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e67e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e67e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e67e-119">-InputObject</span></span>
<span data-ttu-id="6e67e-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6e67e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e67e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e67e-121">-Name</span></span>
<span data-ttu-id="6e67e-122">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="6e67e-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6e67e-123">-NoWait</span></span>
<span data-ttu-id="6e67e-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6e67e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e67e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e67e-125">-PassThru</span></span>
<span data-ttu-id="6e67e-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="6e67e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6e67e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e67e-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e67e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e67e-128">The name of the resource group.</span></span>
<span data-ttu-id="6e67e-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6e67e-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6e67e-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6e67e-130">-ServerName</span></span>
<span data-ttu-id="6e67e-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-131">The name of the server.</span></span>

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

### <span data-ttu-id="6e67e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e67e-132">-SubscriptionId</span></span>
<span data-ttu-id="6e67e-133">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6e67e-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6e67e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e67e-134">-Confirm</span></span>
<span data-ttu-id="6e67e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e67e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e67e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e67e-136">-WhatIf</span></span>
<span data-ttu-id="6e67e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e67e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e67e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e67e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e67e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e67e-139">CommonParameters</span></span>
<span data-ttu-id="6e67e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e67e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e67e-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e67e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e67e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e67e-142">INPUTS</span></span>

### <span data-ttu-id="6e67e-143">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6e67e-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6e67e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e67e-144">OUTPUTS</span></span>

### <span data-ttu-id="6e67e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e67e-145">System.Boolean</span></span>

## <span data-ttu-id="6e67e-146">Note</span><span class="sxs-lookup"><span data-stu-id="6e67e-146">NOTES</span></span>

<span data-ttu-id="6e67e-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6e67e-147">ALIASES</span></span>

<span data-ttu-id="6e67e-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e67e-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e67e-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6e67e-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e67e-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e67e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e67e-151">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6e67e-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e67e-152">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6e67e-153">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="6e67e-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6e67e-154">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6e67e-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6e67e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e67e-156">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="6e67e-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6e67e-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e67e-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6e67e-158">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6e67e-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="6e67e-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6e67e-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6e67e-160">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="6e67e-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6e67e-161">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6e67e-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6e67e-162">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e67e-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6e67e-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e67e-163">RELATED LINKS</span></span>

