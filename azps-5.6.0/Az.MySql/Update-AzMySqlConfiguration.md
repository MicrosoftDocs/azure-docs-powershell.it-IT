---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: bff7f24ef88c8f6fc5022aae019a9c6f32bf95f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968798"
---
# <span data-ttu-id="10ebf-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="10ebf-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="10ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="10ebf-103">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="10ebf-104">Usare Update-AzMySqlServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="10ebf-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="10ebf-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10ebf-105">SYNTAX</span></span>

### <span data-ttu-id="10ebf-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10ebf-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10ebf-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="10ebf-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10ebf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10ebf-108">DESCRIPTION</span></span>
<span data-ttu-id="10ebf-109">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="10ebf-110">Usare Update-AzMySqlServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="10ebf-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="10ebf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10ebf-111">EXAMPLES</span></span>

### <span data-ttu-id="10ebf-112">Esempio 1: Aggiornare la configurazione MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="10ebf-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="10ebf-113">Questo cmdlet aggiorna la configurazione mySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="10ebf-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="10ebf-114">Esempio 2: Aggiornare la configurazione di MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="10ebf-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="10ebf-115">Questi cmdlet aggiornano la configurazione di MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="10ebf-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="10ebf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10ebf-116">PARAMETERS</span></span>

### <span data-ttu-id="10ebf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10ebf-117">-AsJob</span></span>
<span data-ttu-id="10ebf-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="10ebf-118">Run the command as a job</span></span>

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

### <span data-ttu-id="10ebf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ebf-119">-DefaultProfile</span></span>
<span data-ttu-id="10ebf-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10ebf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ebf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10ebf-121">-InputObject</span></span>
<span data-ttu-id="10ebf-122">Parametro identity.</span><span class="sxs-lookup"><span data-stu-id="10ebf-122">Identity Parameter.</span></span>
<span data-ttu-id="10ebf-123">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="10ebf-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10ebf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="10ebf-124">-Name</span></span>
<span data-ttu-id="10ebf-125">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="10ebf-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="10ebf-126">-NoWait</span></span>
<span data-ttu-id="10ebf-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="10ebf-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="10ebf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ebf-128">-ResourceGroupName</span></span>
<span data-ttu-id="10ebf-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10ebf-129">The name of the resource group.</span></span>
<span data-ttu-id="10ebf-130">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="10ebf-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="10ebf-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10ebf-131">-ServerName</span></span>
<span data-ttu-id="10ebf-132">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-132">The name of the server.</span></span>

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

### <span data-ttu-id="10ebf-133">-Source</span><span class="sxs-lookup"><span data-stu-id="10ebf-133">-Source</span></span>
<span data-ttu-id="10ebf-134">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="10ebf-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="10ebf-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10ebf-135">-SubscriptionId</span></span>
<span data-ttu-id="10ebf-136">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="10ebf-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="10ebf-137">-Value</span><span class="sxs-lookup"><span data-stu-id="10ebf-137">-Value</span></span>
<span data-ttu-id="10ebf-138">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="10ebf-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="10ebf-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10ebf-139">-Confirm</span></span>
<span data-ttu-id="10ebf-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ebf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ebf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ebf-141">-WhatIf</span></span>
<span data-ttu-id="10ebf-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10ebf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ebf-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10ebf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ebf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ebf-144">CommonParameters</span></span>
<span data-ttu-id="10ebf-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ebf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ebf-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10ebf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ebf-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="10ebf-147">INPUTS</span></span>

### <span data-ttu-id="10ebf-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="10ebf-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="10ebf-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10ebf-149">OUTPUTS</span></span>

### <span data-ttu-id="10ebf-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="10ebf-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="10ebf-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="10ebf-151">NOTES</span></span>

<span data-ttu-id="10ebf-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="10ebf-152">ALIASES</span></span>

<span data-ttu-id="10ebf-153">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="10ebf-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10ebf-154">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="10ebf-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10ebf-155">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10ebf-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10ebf-156"><IMySqlIdentity>INPUTOBJECT: parametro identity.</span><span class="sxs-lookup"><span data-stu-id="10ebf-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="10ebf-157">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="10ebf-158">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="10ebf-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="10ebf-159">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="10ebf-160">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="10ebf-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10ebf-161">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="10ebf-162">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="10ebf-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="10ebf-163">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10ebf-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="10ebf-164">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="10ebf-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="10ebf-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="10ebf-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="10ebf-166">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="10ebf-167">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="10ebf-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="10ebf-168">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="10ebf-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10ebf-169">RELATED LINKS</span></span>

