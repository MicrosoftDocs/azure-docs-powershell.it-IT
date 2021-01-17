---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475777"
---
# <span data-ttu-id="81b00-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="81b00-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="81b00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81b00-102">SYNOPSIS</span></span>
<span data-ttu-id="81b00-103">Elimina la regola di rete virtuale con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="81b00-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="81b00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81b00-104">SYNTAX</span></span>

### <span data-ttu-id="81b00-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81b00-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="81b00-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81b00-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81b00-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81b00-107">DESCRIPTION</span></span>
<span data-ttu-id="81b00-108">Elimina la regola di rete virtuale con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="81b00-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="81b00-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81b00-109">EXAMPLES</span></span>

### <span data-ttu-id="81b00-110">Esempio 1: rimuovere la regola di rete virtuale del server PostgreSql per nome</span><span class="sxs-lookup"><span data-stu-id="81b00-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="81b00-111">Questo cmdlet rimuove la regola di rete virtuale del server PostgreSql per nome.</span><span class="sxs-lookup"><span data-stu-id="81b00-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="81b00-112">Esempio 2: rimuovere la regola di rete virtuale del server PostgreSql per identità</span><span class="sxs-lookup"><span data-stu-id="81b00-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="81b00-113">Questi cmdlet rimuovono la regola della rete virtuale del server PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="81b00-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="81b00-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81b00-114">PARAMETERS</span></span>

### <span data-ttu-id="81b00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81b00-115">-AsJob</span></span>
<span data-ttu-id="81b00-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="81b00-116">Run the command as a job</span></span>

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

### <span data-ttu-id="81b00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b00-117">-DefaultProfile</span></span>
<span data-ttu-id="81b00-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81b00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81b00-119">-InputObject</span></span>
<span data-ttu-id="81b00-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="81b00-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81b00-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="81b00-121">-Name</span></span>
<span data-ttu-id="81b00-122">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="81b00-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b00-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="81b00-123">-NoWait</span></span>
<span data-ttu-id="81b00-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="81b00-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="81b00-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81b00-125">-PassThru</span></span>
<span data-ttu-id="81b00-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="81b00-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="81b00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b00-127">-ResourceGroupName</span></span>
<span data-ttu-id="81b00-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81b00-128">The name of the resource group.</span></span>
<span data-ttu-id="81b00-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="81b00-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="81b00-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="81b00-130">-ServerName</span></span>
<span data-ttu-id="81b00-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="81b00-131">The name of the server.</span></span>

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

### <span data-ttu-id="81b00-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81b00-132">-SubscriptionId</span></span>
<span data-ttu-id="81b00-133">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="81b00-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="81b00-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81b00-134">-Confirm</span></span>
<span data-ttu-id="81b00-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b00-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b00-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b00-136">-WhatIf</span></span>
<span data-ttu-id="81b00-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81b00-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b00-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81b00-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b00-139">CommonParameters</span></span>
<span data-ttu-id="81b00-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b00-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81b00-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b00-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81b00-142">INPUTS</span></span>

### <span data-ttu-id="81b00-143">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="81b00-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="81b00-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81b00-144">OUTPUTS</span></span>

### <span data-ttu-id="81b00-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81b00-145">System.Boolean</span></span>

## <span data-ttu-id="81b00-146">Note</span><span class="sxs-lookup"><span data-stu-id="81b00-146">NOTES</span></span>

<span data-ttu-id="81b00-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="81b00-147">ALIASES</span></span>

<span data-ttu-id="81b00-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81b00-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81b00-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="81b00-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81b00-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81b00-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81b00-151">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="81b00-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81b00-152">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="81b00-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="81b00-153">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="81b00-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="81b00-154">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="81b00-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="81b00-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="81b00-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81b00-156">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="81b00-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="81b00-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81b00-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="81b00-158">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="81b00-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="81b00-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="81b00-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="81b00-160">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="81b00-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="81b00-161">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="81b00-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="81b00-162">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="81b00-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="81b00-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81b00-163">RELATED LINKS</span></span>

