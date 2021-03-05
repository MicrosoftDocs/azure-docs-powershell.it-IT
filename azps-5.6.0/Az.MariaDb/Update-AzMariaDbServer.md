---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0db4d25f224f1c6984ba9b57184859e8fa2c6c28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003869"
---
# <span data-ttu-id="d75e2-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d75e2-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="d75e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d75e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d75e2-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="d75e2-103">Updates an existing server.</span></span>
<span data-ttu-id="d75e2-104">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella normale definizione del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d75e2-105">Usare Update-AzMariaDbConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d75e2-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d75e2-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d75e2-106">SYNTAX</span></span>

### <span data-ttu-id="d75e2-107">ServerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d75e2-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d75e2-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="d75e2-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d75e2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d75e2-109">DESCRIPTION</span></span>
<span data-ttu-id="d75e2-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="d75e2-110">Updates an existing server.</span></span>
<span data-ttu-id="d75e2-111">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella normale definizione del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d75e2-112">Usare Update-AzMariaDbConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d75e2-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d75e2-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d75e2-113">EXAMPLES</span></span>

### <span data-ttu-id="d75e2-114">Esempio 1: Aggiornare MariaDB</span><span class="sxs-lookup"><span data-stu-id="d75e2-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="d75e2-115">Questo comando aggiorna un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d75e2-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="d75e2-116">Esempio 2: Aggiornare MariaDB</span><span class="sxs-lookup"><span data-stu-id="d75e2-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="d75e2-117">Questo comando aggiorna un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d75e2-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="d75e2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d75e2-118">PARAMETERS</span></span>

### <span data-ttu-id="d75e2-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d75e2-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d75e2-120">Password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="d75e2-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="d75e2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d75e2-121">-AsJob</span></span>
<span data-ttu-id="d75e2-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d75e2-122">Run the command as a job</span></span>

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

### <span data-ttu-id="d75e2-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="d75e2-123">-BackupRetentionDay</span></span>
<span data-ttu-id="d75e2-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="d75e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75e2-125">-DefaultProfile</span></span>
<span data-ttu-id="d75e2-126">region DefaultParameters Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="d75e2-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d75e2-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="d75e2-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="d75e2-128">Abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d75e2-129">-InputObject</span></span>
<span data-ttu-id="d75e2-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d75e2-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d75e2-131">-Name</span></span>
<span data-ttu-id="d75e2-132">Nome del server MariaDB</span><span class="sxs-lookup"><span data-stu-id="d75e2-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d75e2-133">-NoWait</span></span>
<span data-ttu-id="d75e2-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d75e2-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d75e2-135">-ReplicaRole</span><span class="sxs-lookup"><span data-stu-id="d75e2-135">-ReplicationRole</span></span>
<span data-ttu-id="d75e2-136">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="d75e2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d75e2-137">-ResourceGroupName</span></span>
<span data-ttu-id="d75e2-138">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d75e2-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="d75e2-139">-Sku</span></span>
<span data-ttu-id="d75e2-140">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d75e2-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="d75e2-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="d75e2-141">-SslEnforcement</span></span>
<span data-ttu-id="d75e2-142">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="d75e2-143">-StorageAutogrow</span></span>
<span data-ttu-id="d75e2-144">Abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d75e2-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="d75e2-145">-StorageInMb</span></span>
<span data-ttu-id="d75e2-146">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="d75e2-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d75e2-147">-SubscriptionId</span></span>
<span data-ttu-id="d75e2-148">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="d75e2-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75e2-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="d75e2-149">-Tag</span></span>
<span data-ttu-id="d75e2-150">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="d75e2-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d75e2-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d75e2-151">-Confirm</span></span>
<span data-ttu-id="d75e2-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75e2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d75e2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75e2-153">-WhatIf</span></span>
<span data-ttu-id="d75e2-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d75e2-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d75e2-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d75e2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d75e2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75e2-156">CommonParameters</span></span>
<span data-ttu-id="d75e2-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75e2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75e2-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d75e2-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75e2-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="d75e2-159">INPUTS</span></span>

### <span data-ttu-id="d75e2-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d75e2-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d75e2-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d75e2-161">OUTPUTS</span></span>

### <span data-ttu-id="d75e2-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="d75e2-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d75e2-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="d75e2-163">NOTES</span></span>

<span data-ttu-id="d75e2-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d75e2-164">ALIASES</span></span>

<span data-ttu-id="d75e2-165">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d75e2-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d75e2-166">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d75e2-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d75e2-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d75e2-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d75e2-168">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d75e2-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d75e2-169">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d75e2-170">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="d75e2-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d75e2-171">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d75e2-172">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d75e2-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d75e2-173">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d75e2-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d75e2-174">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d75e2-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d75e2-175">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="d75e2-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d75e2-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d75e2-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d75e2-177">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="d75e2-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d75e2-178">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d75e2-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d75e2-179">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d75e2-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d75e2-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d75e2-180">RELATED LINKS</span></span>

