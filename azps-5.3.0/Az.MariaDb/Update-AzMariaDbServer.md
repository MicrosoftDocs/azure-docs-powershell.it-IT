---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475226"
---
# <span data-ttu-id="18bd7-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="18bd7-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="18bd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="18bd7-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="18bd7-103">Updates an existing server.</span></span>
<span data-ttu-id="18bd7-104">Il corpo della richiesta può contenere uno a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="18bd7-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="18bd7-105">USA invece Update-AzMariaDbConfiguration se vuoi aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="18bd7-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="18bd7-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18bd7-106">SYNTAX</span></span>

### <span data-ttu-id="18bd7-107">Nomeserver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18bd7-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18bd7-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="18bd7-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18bd7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18bd7-109">DESCRIPTION</span></span>
<span data-ttu-id="18bd7-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="18bd7-110">Updates an existing server.</span></span>
<span data-ttu-id="18bd7-111">Il corpo della richiesta può contenere uno a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="18bd7-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="18bd7-112">USA invece Update-AzMariaDbConfiguration se vuoi aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="18bd7-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="18bd7-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18bd7-113">EXAMPLES</span></span>

### <span data-ttu-id="18bd7-114">Esempio 1: aggiornare MariaDB</span><span class="sxs-lookup"><span data-stu-id="18bd7-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="18bd7-115">Questo comando aggiorna un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="18bd7-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="18bd7-116">Esempio 2: aggiornare MariaDB</span><span class="sxs-lookup"><span data-stu-id="18bd7-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="18bd7-117">Questo comando aggiorna un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="18bd7-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="18bd7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18bd7-118">PARAMETERS</span></span>

### <span data-ttu-id="18bd7-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="18bd7-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="18bd7-120">La password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="18bd7-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="18bd7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18bd7-121">-AsJob</span></span>
<span data-ttu-id="18bd7-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="18bd7-122">Run the command as a job</span></span>

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

### <span data-ttu-id="18bd7-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="18bd7-123">-BackupRetentionDay</span></span>
<span data-ttu-id="18bd7-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="18bd7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bd7-125">-DefaultProfile</span></span>
<span data-ttu-id="18bd7-126">Region DefaultParameters le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18bd7-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18bd7-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="18bd7-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="18bd7-128">Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="18bd7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18bd7-129">-InputObject</span></span>
<span data-ttu-id="18bd7-130">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="18bd7-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18bd7-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="18bd7-131">-Name</span></span>
<span data-ttu-id="18bd7-132">Nome server MariaDB</span><span class="sxs-lookup"><span data-stu-id="18bd7-132">MariaDB server name</span></span>

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

### <span data-ttu-id="18bd7-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="18bd7-133">-NoWait</span></span>
<span data-ttu-id="18bd7-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="18bd7-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18bd7-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="18bd7-135">-ReplicationRole</span></span>
<span data-ttu-id="18bd7-136">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="18bd7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bd7-137">-ResourceGroupName</span></span>
<span data-ttu-id="18bd7-138">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="18bd7-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="18bd7-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="18bd7-139">-Sku</span></span>
<span data-ttu-id="18bd7-140">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="18bd7-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="18bd7-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="18bd7-141">-SslEnforcement</span></span>
<span data-ttu-id="18bd7-142">Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="18bd7-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="18bd7-143">-StorageAutogrow</span></span>
<span data-ttu-id="18bd7-144">Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18bd7-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="18bd7-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="18bd7-145">-StorageInMb</span></span>
<span data-ttu-id="18bd7-146">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="18bd7-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18bd7-147">-SubscriptionId</span></span>
<span data-ttu-id="18bd7-148">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="18bd7-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="18bd7-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="18bd7-149">-Tag</span></span>
<span data-ttu-id="18bd7-150">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="18bd7-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="18bd7-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18bd7-151">-Confirm</span></span>
<span data-ttu-id="18bd7-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18bd7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18bd7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18bd7-153">-WhatIf</span></span>
<span data-ttu-id="18bd7-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18bd7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18bd7-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18bd7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18bd7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bd7-156">CommonParameters</span></span>
<span data-ttu-id="18bd7-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18bd7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bd7-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18bd7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bd7-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18bd7-159">INPUTS</span></span>

### <span data-ttu-id="18bd7-160">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="18bd7-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="18bd7-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18bd7-161">OUTPUTS</span></span>

### <span data-ttu-id="18bd7-162">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="18bd7-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="18bd7-163">Note</span><span class="sxs-lookup"><span data-stu-id="18bd7-163">NOTES</span></span>

<span data-ttu-id="18bd7-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="18bd7-164">ALIASES</span></span>

<span data-ttu-id="18bd7-165">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18bd7-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18bd7-166">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="18bd7-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18bd7-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18bd7-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18bd7-168">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="18bd7-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18bd7-169">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="18bd7-170">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="18bd7-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="18bd7-171">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="18bd7-172">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="18bd7-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18bd7-173">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="18bd7-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="18bd7-174">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="18bd7-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="18bd7-175">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="18bd7-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="18bd7-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="18bd7-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="18bd7-177">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="18bd7-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="18bd7-178">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="18bd7-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="18bd7-179">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="18bd7-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="18bd7-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18bd7-180">RELATED LINKS</span></span>

