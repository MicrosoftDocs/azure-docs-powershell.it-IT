---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191484"
---
# <span data-ttu-id="14512-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="14512-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="14512-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14512-102">SYNOPSIS</span></span>
<span data-ttu-id="14512-103">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="14512-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="14512-104">Usare Update-AzMariaDbServer invece se si vuole aggiornare AdministratorLoginPassword, SKU e così via.</span><span class="sxs-lookup"><span data-stu-id="14512-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="14512-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14512-105">SYNTAX</span></span>

### <span data-ttu-id="14512-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14512-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14512-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="14512-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14512-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14512-108">DESCRIPTION</span></span>
<span data-ttu-id="14512-109">Aggiorna una configurazione di un server.</span><span class="sxs-lookup"><span data-stu-id="14512-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="14512-110">Usare Update-AzMariaDberver invece se si vuole aggiornare AdministratorLoginPassword, SKU e così via.</span><span class="sxs-lookup"><span data-stu-id="14512-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="14512-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14512-111">EXAMPLES</span></span>

### <span data-ttu-id="14512-112">Esempio 1: aggiornare la configurazione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="14512-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="14512-113">Questo comando aggiorna una configurazione MariaDB.</span><span class="sxs-lookup"><span data-stu-id="14512-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="14512-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14512-114">PARAMETERS</span></span>

### <span data-ttu-id="14512-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14512-115">-AsJob</span></span>
<span data-ttu-id="14512-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="14512-116">Run the command as a job</span></span>

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

### <span data-ttu-id="14512-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14512-117">-DefaultProfile</span></span>
<span data-ttu-id="14512-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14512-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14512-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14512-119">-InputObject</span></span>
<span data-ttu-id="14512-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="14512-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14512-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="14512-121">-Name</span></span>
<span data-ttu-id="14512-122">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="14512-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="14512-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="14512-123">-NoWait</span></span>
<span data-ttu-id="14512-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="14512-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14512-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14512-125">-ResourceGroupName</span></span>
<span data-ttu-id="14512-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="14512-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="14512-127">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="14512-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="14512-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="14512-128">-ServerName</span></span>
<span data-ttu-id="14512-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="14512-129">The name of the server.</span></span>

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

### <span data-ttu-id="14512-130">-Origine</span><span class="sxs-lookup"><span data-stu-id="14512-130">-Source</span></span>
<span data-ttu-id="14512-131">Origine della configurazione.</span><span class="sxs-lookup"><span data-stu-id="14512-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="14512-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14512-132">-SubscriptionId</span></span>
<span data-ttu-id="14512-133">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="14512-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="14512-134">-Valore</span><span class="sxs-lookup"><span data-stu-id="14512-134">-Value</span></span>
<span data-ttu-id="14512-135">Valore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="14512-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="14512-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14512-136">-Confirm</span></span>
<span data-ttu-id="14512-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14512-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14512-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14512-138">-WhatIf</span></span>
<span data-ttu-id="14512-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14512-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14512-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14512-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14512-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14512-141">CommonParameters</span></span>
<span data-ttu-id="14512-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14512-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14512-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14512-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14512-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14512-144">INPUTS</span></span>

### <span data-ttu-id="14512-145">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="14512-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="14512-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14512-146">OUTPUTS</span></span>

### <span data-ttu-id="14512-147">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="14512-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="14512-148">Note</span><span class="sxs-lookup"><span data-stu-id="14512-148">NOTES</span></span>

<span data-ttu-id="14512-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="14512-149">ALIASES</span></span>

<span data-ttu-id="14512-150">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14512-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14512-151">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="14512-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14512-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14512-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14512-153">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="14512-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14512-154">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="14512-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="14512-155">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="14512-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="14512-156">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="14512-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="14512-157">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="14512-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14512-158">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="14512-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="14512-159">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="14512-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="14512-160">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="14512-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="14512-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="14512-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="14512-162">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="14512-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="14512-163">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="14512-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="14512-164">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="14512-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="14512-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14512-165">RELATED LINKS</span></span>

