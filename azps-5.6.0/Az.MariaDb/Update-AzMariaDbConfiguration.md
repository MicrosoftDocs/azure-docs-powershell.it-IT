---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: dc2a36a9ac8c2595ef2f60b8edc40582ad864ff8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003886"
---
# <span data-ttu-id="4c862-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c862-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="4c862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c862-102">SYNOPSIS</span></span>
<span data-ttu-id="4c862-103">Aggiorna la configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="4c862-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="4c862-104">Usare Update-AzMariaDbServer se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="4c862-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4c862-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c862-105">SYNTAX</span></span>

### <span data-ttu-id="4c862-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c862-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4c862-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4c862-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4c862-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c862-108">DESCRIPTION</span></span>
<span data-ttu-id="4c862-109">Aggiorna la configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="4c862-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="4c862-110">Usare Update-AzMariaDberver se si vuole aggiornare AdministratorLoginPassword, sku e così via.</span><span class="sxs-lookup"><span data-stu-id="4c862-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4c862-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c862-111">EXAMPLES</span></span>

### <span data-ttu-id="4c862-112">Esempio 1: Aggiornare la configurazione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="4c862-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="4c862-113">Questo comando aggiorna una configurazione di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4c862-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="4c862-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c862-114">PARAMETERS</span></span>

### <span data-ttu-id="4c862-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c862-115">-AsJob</span></span>
<span data-ttu-id="4c862-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4c862-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4c862-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c862-117">-DefaultProfile</span></span>
<span data-ttu-id="4c862-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c862-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c862-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c862-119">-InputObject</span></span>
<span data-ttu-id="4c862-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4c862-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c862-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4c862-121">-Name</span></span>
<span data-ttu-id="4c862-122">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="4c862-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4c862-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4c862-123">-NoWait</span></span>
<span data-ttu-id="4c862-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4c862-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4c862-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c862-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c862-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c862-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4c862-127">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="4c862-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4c862-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c862-128">-ServerName</span></span>
<span data-ttu-id="4c862-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="4c862-129">The name of the server.</span></span>

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

### <span data-ttu-id="4c862-130">-Source</span><span class="sxs-lookup"><span data-stu-id="4c862-130">-Source</span></span>
<span data-ttu-id="4c862-131">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="4c862-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="4c862-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c862-132">-SubscriptionId</span></span>
<span data-ttu-id="4c862-133">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c862-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4c862-134">-Value</span><span class="sxs-lookup"><span data-stu-id="4c862-134">-Value</span></span>
<span data-ttu-id="4c862-135">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="4c862-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="4c862-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c862-136">-Confirm</span></span>
<span data-ttu-id="4c862-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c862-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c862-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c862-138">-WhatIf</span></span>
<span data-ttu-id="4c862-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c862-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c862-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c862-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c862-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c862-141">CommonParameters</span></span>
<span data-ttu-id="4c862-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c862-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c862-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c862-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c862-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c862-144">INPUTS</span></span>

### <span data-ttu-id="4c862-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4c862-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4c862-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c862-146">OUTPUTS</span></span>

### <span data-ttu-id="4c862-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c862-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="4c862-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c862-148">NOTES</span></span>

<span data-ttu-id="4c862-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4c862-149">ALIASES</span></span>

<span data-ttu-id="4c862-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4c862-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4c862-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4c862-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c862-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c862-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4c862-153">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="4c862-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4c862-154">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="4c862-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4c862-155">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="4c862-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4c862-156">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="4c862-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4c862-157">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4c862-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4c862-158">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="4c862-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4c862-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c862-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4c862-160">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="4c862-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4c862-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4c862-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4c862-162">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="4c862-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4c862-163">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c862-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4c862-164">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4c862-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4c862-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c862-165">RELATED LINKS</span></span>

