---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476112"
---
# <span data-ttu-id="a69af-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="a69af-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="a69af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a69af-102">SYNOPSIS</span></span>
<span data-ttu-id="a69af-103">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="a69af-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="a69af-104">Usare Update-AzMariaDbServer invece se si vuole aggiornare AdministratorLoginPassword, SKU e così via.</span><span class="sxs-lookup"><span data-stu-id="a69af-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="a69af-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a69af-105">SYNTAX</span></span>

### <span data-ttu-id="a69af-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a69af-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a69af-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a69af-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a69af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a69af-108">DESCRIPTION</span></span>
<span data-ttu-id="a69af-109">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="a69af-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="a69af-110">Usare Update-AzMariaDberver invece se si vuole aggiornare AdministratorLoginPassword, SKU e così via.</span><span class="sxs-lookup"><span data-stu-id="a69af-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="a69af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a69af-111">EXAMPLES</span></span>

### <span data-ttu-id="a69af-112">Esempio 1: aggiornare la configurazione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="a69af-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="a69af-113">Questo comando aggiorna una configurazione MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a69af-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="a69af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a69af-114">PARAMETERS</span></span>

### <span data-ttu-id="a69af-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a69af-115">-AsJob</span></span>
<span data-ttu-id="a69af-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a69af-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a69af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69af-117">-DefaultProfile</span></span>
<span data-ttu-id="a69af-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a69af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a69af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a69af-119">-InputObject</span></span>
<span data-ttu-id="a69af-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a69af-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a69af-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a69af-121">-Name</span></span>
<span data-ttu-id="a69af-122">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="a69af-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a69af-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="a69af-123">-NoWait</span></span>
<span data-ttu-id="a69af-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a69af-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a69af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69af-125">-ResourceGroupName</span></span>
<span data-ttu-id="a69af-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69af-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a69af-127">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="a69af-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a69af-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a69af-128">-ServerName</span></span>
<span data-ttu-id="a69af-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="a69af-129">The name of the server.</span></span>

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

### <span data-ttu-id="a69af-130">-Origine</span><span class="sxs-lookup"><span data-stu-id="a69af-130">-Source</span></span>
<span data-ttu-id="a69af-131">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="a69af-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="a69af-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a69af-132">-SubscriptionId</span></span>
<span data-ttu-id="a69af-133">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="a69af-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a69af-134">-Valore</span><span class="sxs-lookup"><span data-stu-id="a69af-134">-Value</span></span>
<span data-ttu-id="a69af-135">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="a69af-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="a69af-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a69af-136">-Confirm</span></span>
<span data-ttu-id="a69af-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a69af-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69af-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69af-138">-WhatIf</span></span>
<span data-ttu-id="a69af-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a69af-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a69af-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a69af-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69af-141">CommonParameters</span></span>
<span data-ttu-id="a69af-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69af-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a69af-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69af-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a69af-144">INPUTS</span></span>

### <span data-ttu-id="a69af-145">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a69af-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a69af-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a69af-146">OUTPUTS</span></span>

### <span data-ttu-id="a69af-147">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="a69af-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="a69af-148">Note</span><span class="sxs-lookup"><span data-stu-id="a69af-148">NOTES</span></span>

<span data-ttu-id="a69af-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a69af-149">ALIASES</span></span>

<span data-ttu-id="a69af-150">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a69af-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a69af-151">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a69af-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a69af-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a69af-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a69af-153">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a69af-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a69af-154">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="a69af-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a69af-155">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="a69af-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a69af-156">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="a69af-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a69af-157">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a69af-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a69af-158">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="a69af-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a69af-159">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69af-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a69af-160">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="a69af-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a69af-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a69af-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a69af-162">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="a69af-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a69af-163">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="a69af-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a69af-164">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a69af-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a69af-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a69af-165">RELATED LINKS</span></span>

