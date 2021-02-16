---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194150"
---
# <span data-ttu-id="33c9f-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="33c9f-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="33c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="33c9f-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="33c9f-103">Updates an existing server.</span></span>
<span data-ttu-id="33c9f-104">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="33c9f-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="33c9f-105">Usare Update-AzMariaDbConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="33c9f-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="33c9f-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33c9f-106">SYNTAX</span></span>

### <span data-ttu-id="33c9f-107">ServerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33c9f-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33c9f-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="33c9f-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33c9f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33c9f-109">DESCRIPTION</span></span>
<span data-ttu-id="33c9f-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="33c9f-110">Updates an existing server.</span></span>
<span data-ttu-id="33c9f-111">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="33c9f-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="33c9f-112">Usare Update-AzMariaDbConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="33c9f-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="33c9f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33c9f-113">EXAMPLES</span></span>

### <span data-ttu-id="33c9f-114">Esempio 1: Aggiornare MariaDB</span><span class="sxs-lookup"><span data-stu-id="33c9f-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="33c9f-115">Questo comando aggiorna un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="33c9f-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="33c9f-116">Esempio 2: Aggiornare MariaDB</span><span class="sxs-lookup"><span data-stu-id="33c9f-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="33c9f-117">Questo comando aggiorna un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="33c9f-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="33c9f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33c9f-118">PARAMETERS</span></span>

### <span data-ttu-id="33c9f-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="33c9f-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="33c9f-120">Password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="33c9f-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="33c9f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33c9f-121">-AsJob</span></span>
<span data-ttu-id="33c9f-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="33c9f-122">Run the command as a job</span></span>

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

### <span data-ttu-id="33c9f-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="33c9f-123">-BackupRetentionDay</span></span>
<span data-ttu-id="33c9f-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="33c9f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c9f-125">-DefaultProfile</span></span>
<span data-ttu-id="33c9f-126">region DefaultParameters Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="33c9f-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c9f-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="33c9f-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="33c9f-128">Abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="33c9f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33c9f-129">-InputObject</span></span>
<span data-ttu-id="33c9f-130">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="33c9f-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="33c9f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="33c9f-131">-Name</span></span>
<span data-ttu-id="33c9f-132">Nome server MariaDB</span><span class="sxs-lookup"><span data-stu-id="33c9f-132">MariaDB server name</span></span>

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

### <span data-ttu-id="33c9f-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33c9f-133">-NoWait</span></span>
<span data-ttu-id="33c9f-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="33c9f-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33c9f-135">-ReplicaRole</span><span class="sxs-lookup"><span data-stu-id="33c9f-135">-ReplicationRole</span></span>
<span data-ttu-id="33c9f-136">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="33c9f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c9f-137">-ResourceGroupName</span></span>
<span data-ttu-id="33c9f-138">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="33c9f-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="33c9f-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="33c9f-139">-Sku</span></span>
<span data-ttu-id="33c9f-140">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="33c9f-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="33c9f-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="33c9f-141">-SslEnforcement</span></span>
<span data-ttu-id="33c9f-142">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="33c9f-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="33c9f-143">-StorageAutogrow</span></span>
<span data-ttu-id="33c9f-144">Abilitare l'estensione automatica dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33c9f-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="33c9f-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="33c9f-145">-StorageInMb</span></span>
<span data-ttu-id="33c9f-146">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="33c9f-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33c9f-147">-SubscriptionId</span></span>
<span data-ttu-id="33c9f-148">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="33c9f-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="33c9f-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="33c9f-149">-Tag</span></span>
<span data-ttu-id="33c9f-150">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="33c9f-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="33c9f-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33c9f-151">-Confirm</span></span>
<span data-ttu-id="33c9f-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c9f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c9f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c9f-153">-WhatIf</span></span>
<span data-ttu-id="33c9f-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33c9f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33c9f-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33c9f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c9f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c9f-156">CommonParameters</span></span>
<span data-ttu-id="33c9f-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c9f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c9f-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33c9f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c9f-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="33c9f-159">INPUTS</span></span>

### <span data-ttu-id="33c9f-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="33c9f-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="33c9f-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33c9f-161">OUTPUTS</span></span>

### <span data-ttu-id="33c9f-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="33c9f-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="33c9f-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="33c9f-163">NOTES</span></span>

<span data-ttu-id="33c9f-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33c9f-164">ALIASES</span></span>

<span data-ttu-id="33c9f-165">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="33c9f-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33c9f-166">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="33c9f-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33c9f-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33c9f-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33c9f-168">INPUTOBJECT <IMariaDbIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="33c9f-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33c9f-169">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="33c9f-170">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="33c9f-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="33c9f-171">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="33c9f-172">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="33c9f-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33c9f-173">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="33c9f-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="33c9f-174">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="33c9f-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="33c9f-175">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="33c9f-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="33c9f-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="33c9f-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="33c9f-177">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="33c9f-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="33c9f-178">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="33c9f-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="33c9f-179">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33c9f-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="33c9f-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33c9f-180">RELATED LINKS</span></span>

