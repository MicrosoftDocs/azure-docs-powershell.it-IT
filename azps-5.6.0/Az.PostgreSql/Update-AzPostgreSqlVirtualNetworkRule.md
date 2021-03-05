---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 89c11be18fbb603f2b05fa9768a3ce05d51ddd86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974637"
---
# <span data-ttu-id="d1a80-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d1a80-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="d1a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a80-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a80-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="d1a80-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d1a80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1a80-104">SYNTAX</span></span>

### <span data-ttu-id="d1a80-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1a80-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1a80-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1a80-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1a80-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1a80-107">DESCRIPTION</span></span>
<span data-ttu-id="d1a80-108">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="d1a80-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d1a80-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1a80-109">EXAMPLES</span></span>

### <span data-ttu-id="d1a80-110">Esempio 1: Aggiornare la regola di rete virtuale PostgreSql in base al nome</span><span class="sxs-lookup"><span data-stu-id="d1a80-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="d1a80-111">Questo cmdlet aggiorna la regola della rete virtuale PostgreSql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="d1a80-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="d1a80-112">Esempio 2: Aggiornare la regola di rete virtuale PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d1a80-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="d1a80-113">Questi cmdlet aggiornano la regola della rete virtuale PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d1a80-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="d1a80-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a80-114">PARAMETERS</span></span>

### <span data-ttu-id="d1a80-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1a80-115">-AsJob</span></span>
<span data-ttu-id="d1a80-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d1a80-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d1a80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a80-117">-DefaultProfile</span></span>
<span data-ttu-id="d1a80-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a80-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a80-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1a80-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d1a80-120">Creare una regola del firewall prima che per la rete virtuale sia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="d1a80-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="d1a80-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1a80-121">-InputObject</span></span>
<span data-ttu-id="d1a80-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d1a80-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1a80-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d1a80-123">-Name</span></span>
<span data-ttu-id="d1a80-124">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1a80-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a80-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d1a80-125">-NoWait</span></span>
<span data-ttu-id="d1a80-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d1a80-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1a80-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1a80-127">-PassThru</span></span>
<span data-ttu-id="d1a80-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="d1a80-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d1a80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a80-129">-ResourceGroupName</span></span>
<span data-ttu-id="d1a80-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1a80-130">The name of the resource group.</span></span>
<span data-ttu-id="d1a80-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d1a80-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d1a80-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1a80-132">-ServerName</span></span>
<span data-ttu-id="d1a80-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d1a80-133">The name of the server.</span></span>

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

### <span data-ttu-id="d1a80-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d1a80-134">-SubnetId</span></span>
<span data-ttu-id="d1a80-135">ID ARM della risorsa della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1a80-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a80-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1a80-136">-SubscriptionId</span></span>
<span data-ttu-id="d1a80-137">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1a80-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d1a80-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1a80-138">-Confirm</span></span>
<span data-ttu-id="d1a80-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a80-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a80-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a80-140">-WhatIf</span></span>
<span data-ttu-id="d1a80-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1a80-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a80-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1a80-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a80-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a80-143">CommonParameters</span></span>
<span data-ttu-id="d1a80-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a80-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a80-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1a80-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a80-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1a80-146">INPUTS</span></span>

### <span data-ttu-id="d1a80-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d1a80-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d1a80-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1a80-148">OUTPUTS</span></span>

### <span data-ttu-id="d1a80-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d1a80-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="d1a80-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1a80-150">NOTES</span></span>

<span data-ttu-id="d1a80-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d1a80-151">ALIASES</span></span>

<span data-ttu-id="d1a80-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d1a80-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1a80-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d1a80-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1a80-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1a80-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1a80-155">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d1a80-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1a80-156">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d1a80-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d1a80-157">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="d1a80-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d1a80-158">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d1a80-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d1a80-159">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d1a80-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1a80-160">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d1a80-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d1a80-161">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1a80-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d1a80-162">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d1a80-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="d1a80-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d1a80-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d1a80-164">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="d1a80-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d1a80-165">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1a80-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d1a80-166">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1a80-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d1a80-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1a80-167">RELATED LINKS</span></span>

