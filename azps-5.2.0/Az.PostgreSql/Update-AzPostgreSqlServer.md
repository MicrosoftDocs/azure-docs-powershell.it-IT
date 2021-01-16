---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331144"
---
# <span data-ttu-id="8b757-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="8b757-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="8b757-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b757-102">SYNOPSIS</span></span>
<span data-ttu-id="8b757-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="8b757-103">Updates an existing server.</span></span>
<span data-ttu-id="8b757-104">Il corpo della richiesta può contenere uno a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="8b757-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8b757-105">USA invece Update-AzPostSqlConfiguration se vuoi aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8b757-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8b757-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b757-106">SYNTAX</span></span>

### <span data-ttu-id="8b757-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b757-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b757-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8b757-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b757-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b757-109">DESCRIPTION</span></span>
<span data-ttu-id="8b757-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="8b757-110">Updates an existing server.</span></span>
<span data-ttu-id="8b757-111">Il corpo della richiesta può contenere uno a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="8b757-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8b757-112">USA invece Update-AzPostSqlConfiguration se vuoi aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8b757-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8b757-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b757-113">EXAMPLES</span></span>

### <span data-ttu-id="8b757-114">Esempio 1: aggiornare il server PostgreSql per il gruppo di risorse e il nome del server</span><span class="sxs-lookup"><span data-stu-id="8b757-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8b757-115">Questo cmdlet aggiorna il server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="8b757-116">Esempio 2: aggiornare il server PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="8b757-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8b757-117">Questo cmdlet aggiorna il server PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="8b757-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="8b757-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b757-118">PARAMETERS</span></span>

### <span data-ttu-id="8b757-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8b757-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8b757-120">La password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="8b757-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="8b757-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b757-121">-AsJob</span></span>
<span data-ttu-id="8b757-122">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="8b757-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="8b757-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8b757-123">-BackupRetentionDay</span></span>
<span data-ttu-id="8b757-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="8b757-124">Backup retention days for the server.</span></span>
<span data-ttu-id="8b757-125">Il numero di giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="8b757-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="8b757-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b757-126">-DefaultProfile</span></span>
<span data-ttu-id="8b757-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b757-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b757-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b757-128">-InputObject</span></span>
<span data-ttu-id="8b757-129">Parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="8b757-129">Identity Parameter.</span></span>
<span data-ttu-id="8b757-130">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8b757-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8b757-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b757-131">-Name</span></span>
<span data-ttu-id="8b757-132">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-132">The name of the server.</span></span>

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

### <span data-ttu-id="8b757-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="8b757-133">-NoWait</span></span>
<span data-ttu-id="8b757-134">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="8b757-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8b757-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="8b757-135">-ReplicationRole</span></span>
<span data-ttu-id="8b757-136">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="8b757-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b757-137">-ResourceGroupName</span></span>
<span data-ttu-id="8b757-138">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b757-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8b757-139">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="8b757-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8b757-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="8b757-140">-Sku</span></span>
<span data-ttu-id="8b757-141">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8b757-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8b757-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8b757-142">-SkuCapacity</span></span>
<span data-ttu-id="8b757-143">La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="8b757-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="8b757-144">-SkuFamily</span></span>
<span data-ttu-id="8b757-145">La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="8b757-145">The family of hardware.</span></span>

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

### <span data-ttu-id="8b757-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8b757-146">-SkuTier</span></span>
<span data-ttu-id="8b757-147">Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="8b757-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="8b757-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8b757-148">-SslEnforcement</span></span>
<span data-ttu-id="8b757-149">Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="8b757-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="8b757-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8b757-150">-StorageAutogrow</span></span>
<span data-ttu-id="8b757-151">Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8b757-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="8b757-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8b757-152">-StorageInMb</span></span>
<span data-ttu-id="8b757-153">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="8b757-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8b757-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b757-154">-SubscriptionId</span></span>
<span data-ttu-id="8b757-155">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="8b757-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8b757-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b757-156">-Tag</span></span>
<span data-ttu-id="8b757-157">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="8b757-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8b757-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b757-158">-Confirm</span></span>
<span data-ttu-id="8b757-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b757-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b757-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b757-160">-WhatIf</span></span>
<span data-ttu-id="8b757-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b757-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b757-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b757-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b757-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b757-163">CommonParameters</span></span>
<span data-ttu-id="8b757-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b757-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b757-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b757-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b757-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b757-166">INPUTS</span></span>

### <span data-ttu-id="8b757-167">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8b757-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8b757-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b757-168">OUTPUTS</span></span>

### <span data-ttu-id="8b757-169">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="8b757-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8b757-170">Note</span><span class="sxs-lookup"><span data-stu-id="8b757-170">NOTES</span></span>

<span data-ttu-id="8b757-171">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8b757-171">ALIASES</span></span>

<span data-ttu-id="8b757-172">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b757-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b757-173">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8b757-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b757-174">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b757-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b757-175">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="8b757-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="8b757-176">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8b757-177">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="8b757-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8b757-178">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8b757-179">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8b757-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b757-180">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="8b757-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8b757-181">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b757-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8b757-182">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8b757-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="8b757-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8b757-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8b757-184">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="8b757-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8b757-185">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8b757-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8b757-186">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b757-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8b757-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b757-187">RELATED LINKS</span></span>

