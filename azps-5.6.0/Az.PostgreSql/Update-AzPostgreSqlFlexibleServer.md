---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974669"
---
# <span data-ttu-id="7b2f1-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="7b2f1-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="7b2f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b2f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2f1-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-103">Updates an existing server.</span></span>
<span data-ttu-id="7b2f1-104">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella normale definizione del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="7b2f1-105">Usare Update-AzPostSqlFlexibleServerConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="7b2f1-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b2f1-106">SYNTAX</span></span>

### <span data-ttu-id="7b2f1-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b2f1-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b2f1-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7b2f1-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b2f1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b2f1-109">DESCRIPTION</span></span>
<span data-ttu-id="7b2f1-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-110">Updates an existing server.</span></span>
<span data-ttu-id="7b2f1-111">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella normale definizione del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="7b2f1-112">Usare Update-AzPostgreSqlFlexibleServerConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="7b2f1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b2f1-113">EXAMPLES</span></span>

### <span data-ttu-id="7b2f1-114">Esempio 1: Aggiornare il server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="7b2f1-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="7b2f1-115">Questo cmdlet aggiorna il server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="7b2f1-116">Esempio 2: Aggiornare il server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="7b2f1-117">Questo cmdlet aggiorna il server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="7b2f1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b2f1-118">PARAMETERS</span></span>

### <span data-ttu-id="7b2f1-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7b2f1-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7b2f1-120">Password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b2f1-121">-AsJob</span></span>
<span data-ttu-id="7b2f1-122">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="7b2f1-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="7b2f1-123">-BackupRetentionDay</span></span>
<span data-ttu-id="7b2f1-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-124">Backup retention days for the server.</span></span>
<span data-ttu-id="7b2f1-125">Il numero dei giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2f1-126">-DefaultProfile</span></span>
<span data-ttu-id="7b2f1-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b2f1-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="7b2f1-128">-HaEnabled</span></span>
<span data-ttu-id="7b2f1-129">Abilitare o disabilitare la funzionalità disponibilità elevata.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b2f1-130">-InputObject</span></span>
<span data-ttu-id="7b2f1-131">Parametro identity.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-131">Identity Parameter.</span></span>
<span data-ttu-id="7b2f1-132">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b2f1-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="7b2f1-133">-MaintenanceWindow</span></span>
<span data-ttu-id="7b2f1-134">Periodo di tempo (UTC) designato per la manutenzione.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="7b2f1-135">Esempi: "Dom:23:30" per programmare la domenica, 23:30 UTC.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="7b2f1-136">Per tornare al pass predefinito in "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="7b2f1-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="7b2f1-137">-Name</span><span class="sxs-lookup"><span data-stu-id="7b2f1-137">-Name</span></span>
<span data-ttu-id="7b2f1-138">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-138">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7b2f1-139">-NoWait</span></span>
<span data-ttu-id="7b2f1-140">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="7b2f1-141">-ReplicaRole</span><span class="sxs-lookup"><span data-stu-id="7b2f1-141">-ReplicationRole</span></span>
<span data-ttu-id="7b2f1-142">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="7b2f1-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2f1-143">-ResourceGroupName</span></span>
<span data-ttu-id="7b2f1-144">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7b2f1-145">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7b2f1-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="7b2f1-146">-Sku</span></span>
<span data-ttu-id="7b2f1-147">Il nome della sKU, ad esempio Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="7b2f1-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="7b2f1-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7b2f1-148">-SkuTier</span></span>
<span data-ttu-id="7b2f1-149">Livello dello specifico SKU.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="7b2f1-150">Valori accettati: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="7b2f1-151">Impostazione predefinita: esplosa.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-151">Default: Burstable.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="7b2f1-152">-SslEnforcement</span></span>
<span data-ttu-id="7b2f1-153">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-153">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="7b2f1-154">-StorageAutogrow</span></span>
<span data-ttu-id="7b2f1-155">Abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-155">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="7b2f1-156">-StorageInMb</span></span>
<span data-ttu-id="7b2f1-157">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-157">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b2f1-158">-SubscriptionId</span></span>
<span data-ttu-id="7b2f1-159">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="7b2f1-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b2f1-160">-Tag</span></span>
<span data-ttu-id="7b2f1-161">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-161">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2f1-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b2f1-162">-Confirm</span></span>
<span data-ttu-id="7b2f1-163">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b2f1-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b2f1-164">-WhatIf</span></span>
<span data-ttu-id="7b2f1-165">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b2f1-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b2f1-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2f1-167">CommonParameters</span></span>
<span data-ttu-id="7b2f1-168">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2f1-169">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2f1-170">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b2f1-170">INPUTS</span></span>

### <span data-ttu-id="7b2f1-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7b2f1-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7b2f1-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b2f1-172">OUTPUTS</span></span>

### <span data-ttu-id="7b2f1-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="7b2f1-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="7b2f1-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b2f1-174">NOTES</span></span>

<span data-ttu-id="7b2f1-175">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7b2f1-175">ALIASES</span></span>

<span data-ttu-id="7b2f1-176">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7b2f1-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b2f1-177">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b2f1-178">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b2f1-179"><IPostgreSqlIdentity>INPUTOBJECT: parametro identity.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="7b2f1-180">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7b2f1-181">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7b2f1-182">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7b2f1-183">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="7b2f1-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b2f1-184">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7b2f1-185">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7b2f1-186">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="7b2f1-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7b2f1-188">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7b2f1-189">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7b2f1-190">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b2f1-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7b2f1-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b2f1-191">RELATED LINKS</span></span>

