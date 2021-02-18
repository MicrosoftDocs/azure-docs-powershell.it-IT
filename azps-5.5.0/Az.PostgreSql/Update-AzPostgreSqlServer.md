---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: 4b0d2f01336de83acbd904e08b0d0cbc62c0aca6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202175"
---
# <span data-ttu-id="e3c73-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="e3c73-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="e3c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c73-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c73-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="e3c73-103">Updates an existing server.</span></span>
<span data-ttu-id="e3c73-104">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella normale definizione del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e3c73-105">Usare Update-AzPostSqlConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e3c73-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e3c73-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3c73-106">SYNTAX</span></span>

### <span data-ttu-id="e3c73-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3c73-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3c73-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e3c73-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3c73-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3c73-109">DESCRIPTION</span></span>
<span data-ttu-id="e3c73-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="e3c73-110">Updates an existing server.</span></span>
<span data-ttu-id="e3c73-111">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella normale definizione del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e3c73-112">Usare Update-AzPostSqlConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e3c73-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e3c73-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3c73-113">EXAMPLES</span></span>

### <span data-ttu-id="e3c73-114">Esempio 1: Aggiornare il server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="e3c73-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="e3c73-115">Questo cmdlet aggiorna il server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="e3c73-116">Esempio 2: Aggiornare il server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="e3c73-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="e3c73-117">Questo cmdlet aggiorna il server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="e3c73-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="e3c73-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3c73-118">PARAMETERS</span></span>

### <span data-ttu-id="e3c73-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="e3c73-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="e3c73-120">Password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="e3c73-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="e3c73-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3c73-121">-AsJob</span></span>
<span data-ttu-id="e3c73-122">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="e3c73-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="e3c73-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="e3c73-123">-BackupRetentionDay</span></span>
<span data-ttu-id="e3c73-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-124">Backup retention days for the server.</span></span>
<span data-ttu-id="e3c73-125">Il numero dei giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="e3c73-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="e3c73-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c73-126">-DefaultProfile</span></span>
<span data-ttu-id="e3c73-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c73-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c73-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3c73-128">-InputObject</span></span>
<span data-ttu-id="e3c73-129">Parametro identity.</span><span class="sxs-lookup"><span data-stu-id="e3c73-129">Identity Parameter.</span></span>
<span data-ttu-id="e3c73-130">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e3c73-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3c73-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e3c73-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="e3c73-132">Impostare la versione minima di TLS per le connessioni al server quando è abilitato SSL.</span><span class="sxs-lookup"><span data-stu-id="e3c73-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="e3c73-133">Il valore predefinito è TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="e3c73-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c73-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e3c73-134">-Name</span></span>
<span data-ttu-id="e3c73-135">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-135">The name of the server.</span></span>

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

### <span data-ttu-id="e3c73-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e3c73-136">-NoWait</span></span>
<span data-ttu-id="e3c73-137">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e3c73-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e3c73-138">-ReplicaRole</span><span class="sxs-lookup"><span data-stu-id="e3c73-138">-ReplicationRole</span></span>
<span data-ttu-id="e3c73-139">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="e3c73-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c73-140">-ResourceGroupName</span></span>
<span data-ttu-id="e3c73-141">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3c73-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e3c73-142">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="e3c73-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e3c73-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="e3c73-143">-Sku</span></span>
<span data-ttu-id="e3c73-144">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e3c73-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e3c73-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e3c73-145">-SkuCapacity</span></span>
<span data-ttu-id="e3c73-146">Capacità di scalabilità orizzontale e verticale che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="e3c73-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="e3c73-147">-SkuFamily</span></span>
<span data-ttu-id="e3c73-148">Famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="e3c73-148">The family of hardware.</span></span>

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

### <span data-ttu-id="e3c73-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e3c73-149">-SkuTier</span></span>
<span data-ttu-id="e3c73-150">Livello dello specifico SKU, ad esempio Base.</span><span class="sxs-lookup"><span data-stu-id="e3c73-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="e3c73-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="e3c73-151">-SslEnforcement</span></span>
<span data-ttu-id="e3c73-152">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="e3c73-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="e3c73-153">-StorageAutogrow</span></span>
<span data-ttu-id="e3c73-154">Abilitare l'estensione automatica dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3c73-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="e3c73-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="e3c73-155">-StorageInMb</span></span>
<span data-ttu-id="e3c73-156">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="e3c73-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3c73-157">-SubscriptionId</span></span>
<span data-ttu-id="e3c73-158">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c73-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e3c73-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3c73-159">-Tag</span></span>
<span data-ttu-id="e3c73-160">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="e3c73-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="e3c73-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3c73-161">-Confirm</span></span>
<span data-ttu-id="e3c73-162">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c73-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c73-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c73-163">-WhatIf</span></span>
<span data-ttu-id="e3c73-164">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c73-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c73-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c73-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c73-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c73-166">CommonParameters</span></span>
<span data-ttu-id="e3c73-167">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c73-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c73-168">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3c73-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c73-169">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3c73-169">INPUTS</span></span>

### <span data-ttu-id="e3c73-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e3c73-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e3c73-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3c73-171">OUTPUTS</span></span>

### <span data-ttu-id="e3c73-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e3c73-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e3c73-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3c73-173">NOTES</span></span>

<span data-ttu-id="e3c73-174">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e3c73-174">ALIASES</span></span>

<span data-ttu-id="e3c73-175">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e3c73-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3c73-176">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e3c73-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3c73-177">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3c73-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3c73-178"><IPostgreSqlIdentity>INPUTOBJECT: parametro identity.</span><span class="sxs-lookup"><span data-stu-id="e3c73-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="e3c73-179">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e3c73-180">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="e3c73-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e3c73-181">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e3c73-182">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e3c73-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3c73-183">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e3c73-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e3c73-184">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3c73-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e3c73-185">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e3c73-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="e3c73-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e3c73-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e3c73-187">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="e3c73-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e3c73-188">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3c73-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e3c73-189">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3c73-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e3c73-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3c73-190">RELATED LINKS</span></span>

