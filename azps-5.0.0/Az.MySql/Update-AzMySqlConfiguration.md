---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201861"
---
# <span data-ttu-id="666e4-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="666e4-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="666e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="666e4-102">SYNOPSIS</span></span>
<span data-ttu-id="666e4-103">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="666e4-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="666e4-104">Usare Update-AzMySqlServer invece se si vuole aggiornare AdministratorLoginPassword, SKU e così via.</span><span class="sxs-lookup"><span data-stu-id="666e4-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="666e4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="666e4-105">SYNTAX</span></span>

### <span data-ttu-id="666e4-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="666e4-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="666e4-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="666e4-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="666e4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="666e4-108">DESCRIPTION</span></span>
<span data-ttu-id="666e4-109">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="666e4-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="666e4-110">Usare Update-AzMySqlServer invece se si vuole aggiornare AdministratorLoginPassword, SKU e così via.</span><span class="sxs-lookup"><span data-stu-id="666e4-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="666e4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="666e4-111">EXAMPLES</span></span>

### <span data-ttu-id="666e4-112">Esempio 1: aggiornare la configurazione di MySql per nome</span><span class="sxs-lookup"><span data-stu-id="666e4-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="666e4-113">Questo cmdlet aggiorna la configurazione di MySql per nome.</span><span class="sxs-lookup"><span data-stu-id="666e4-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="666e4-114">Esempio 2: aggiornare la configurazione di MySql per identità.</span><span class="sxs-lookup"><span data-stu-id="666e4-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="666e4-115">Questi cmdlet aggiornano la configurazione di MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="666e4-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="666e4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="666e4-116">PARAMETERS</span></span>

### <span data-ttu-id="666e4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="666e4-117">-AsJob</span></span>
<span data-ttu-id="666e4-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="666e4-118">Run the command as a job</span></span>

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

### <span data-ttu-id="666e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666e4-119">-DefaultProfile</span></span>
<span data-ttu-id="666e4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="666e4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="666e4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="666e4-121">-InputObject</span></span>
<span data-ttu-id="666e4-122">Parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="666e4-122">Identity Parameter.</span></span>
<span data-ttu-id="666e4-123">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="666e4-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="666e4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="666e4-124">-Name</span></span>
<span data-ttu-id="666e4-125">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="666e4-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="666e4-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="666e4-126">-NoWait</span></span>
<span data-ttu-id="666e4-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="666e4-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="666e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="666e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="666e4-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="666e4-129">The name of the resource group.</span></span>
<span data-ttu-id="666e4-130">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="666e4-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="666e4-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="666e4-131">-ServerName</span></span>
<span data-ttu-id="666e4-132">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="666e4-132">The name of the server.</span></span>

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

### <span data-ttu-id="666e4-133">-Origine</span><span class="sxs-lookup"><span data-stu-id="666e4-133">-Source</span></span>
<span data-ttu-id="666e4-134">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="666e4-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="666e4-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="666e4-135">-SubscriptionId</span></span>
<span data-ttu-id="666e4-136">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="666e4-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="666e4-137">-Valore</span><span class="sxs-lookup"><span data-stu-id="666e4-137">-Value</span></span>
<span data-ttu-id="666e4-138">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="666e4-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="666e4-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="666e4-139">-Confirm</span></span>
<span data-ttu-id="666e4-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666e4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666e4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666e4-141">-WhatIf</span></span>
<span data-ttu-id="666e4-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="666e4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="666e4-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="666e4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="666e4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666e4-144">CommonParameters</span></span>
<span data-ttu-id="666e4-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666e4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666e4-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="666e4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666e4-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="666e4-147">INPUTS</span></span>

### <span data-ttu-id="666e4-148">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="666e4-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="666e4-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="666e4-149">OUTPUTS</span></span>

### <span data-ttu-id="666e4-150">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="666e4-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="666e4-151">Note</span><span class="sxs-lookup"><span data-stu-id="666e4-151">NOTES</span></span>

<span data-ttu-id="666e4-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="666e4-152">ALIASES</span></span>

<span data-ttu-id="666e4-153">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="666e4-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="666e4-154">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="666e4-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="666e4-155">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="666e4-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="666e4-156">INPUTOBJECT <IMySqlIdentity> : parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="666e4-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="666e4-157">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="666e4-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="666e4-158">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="666e4-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="666e4-159">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="666e4-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="666e4-160">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="666e4-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="666e4-161">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="666e4-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="666e4-162">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="666e4-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="666e4-163">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="666e4-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="666e4-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="666e4-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="666e4-165">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="666e4-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="666e4-166">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="666e4-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="666e4-167">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="666e4-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="666e4-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="666e4-168">RELATED LINKS</span></span>

