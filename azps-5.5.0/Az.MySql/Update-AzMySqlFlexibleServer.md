---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180030"
---
# <span data-ttu-id="d1f61-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="d1f61-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="d1f61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f61-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f61-103">Aggiorna un server flessibile MySQL esistente.</span><span class="sxs-lookup"><span data-stu-id="d1f61-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="d1f61-104">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="d1f61-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d1f61-105">Usare Update-AzMySqlFlexibleServerConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d1f61-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d1f61-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1f61-106">SYNTAX</span></span>

### <span data-ttu-id="d1f61-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1f61-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1f61-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1f61-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1f61-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1f61-109">DESCRIPTION</span></span>
<span data-ttu-id="d1f61-110">Aggiorna un server flessibile MySQL esistente.</span><span class="sxs-lookup"><span data-stu-id="d1f61-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="d1f61-111">Il corpo della richiesta può contenere da una a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="d1f61-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d1f61-112">Usare Update-AzMySqlFlexibleServerConfiguration invece se si vogliono aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d1f61-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d1f61-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1f61-113">EXAMPLES</span></span>

### <span data-ttu-id="d1f61-114">Esempio 1: Aggiornare il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="d1f61-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="d1f61-115">Questo cmdlet aggiorna il server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="d1f61-116">Esempio 2: Aggiornare il server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d1f61-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="d1f61-117">Questo cmdlet aggiorna il server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d1f61-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="d1f61-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f61-118">PARAMETERS</span></span>

### <span data-ttu-id="d1f61-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d1f61-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d1f61-120">Password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="d1f61-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="d1f61-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1f61-121">-AsJob</span></span>
<span data-ttu-id="d1f61-122">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="d1f61-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="d1f61-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="d1f61-123">-BackupRetentionDay</span></span>
<span data-ttu-id="d1f61-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-124">Backup retention days for the server.</span></span>
<span data-ttu-id="d1f61-125">Il numero dei giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="d1f61-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="d1f61-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f61-126">-DefaultProfile</span></span>
<span data-ttu-id="d1f61-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f61-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f61-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="d1f61-128">-HaEnabled</span></span>
<span data-ttu-id="d1f61-129">Abilitare o disabilitare la funzionalità disponibilità elevata.</span><span class="sxs-lookup"><span data-stu-id="d1f61-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f61-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1f61-130">-InputObject</span></span>
<span data-ttu-id="d1f61-131">Parametro identity.</span><span class="sxs-lookup"><span data-stu-id="d1f61-131">Identity Parameter.</span></span>
<span data-ttu-id="d1f61-132">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d1f61-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1f61-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f61-133">-Name</span></span>
<span data-ttu-id="d1f61-134">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-134">The name of the server.</span></span>

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

### <span data-ttu-id="d1f61-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d1f61-135">-NoWait</span></span>
<span data-ttu-id="d1f61-136">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="d1f61-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d1f61-137">-ReplicaRole</span><span class="sxs-lookup"><span data-stu-id="d1f61-137">-ReplicationRole</span></span>
<span data-ttu-id="d1f61-138">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="d1f61-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f61-139">-ResourceGroupName</span></span>
<span data-ttu-id="d1f61-140">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d1f61-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d1f61-141">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="d1f61-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d1f61-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="d1f61-142">-Sku</span></span>
<span data-ttu-id="d1f61-143">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d1f61-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="d1f61-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d1f61-144">-SkuTier</span></span>
<span data-ttu-id="d1f61-145">Livello dello specifico SKU, ad esempio Base.</span><span class="sxs-lookup"><span data-stu-id="d1f61-145">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f61-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="d1f61-146">-SslEnforcement</span></span>
<span data-ttu-id="d1f61-147">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-147">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f61-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="d1f61-148">-StorageAutogrow</span></span>
<span data-ttu-id="d1f61-149">Abilitare l'estensione automatica dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d1f61-149">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f61-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="d1f61-150">-StorageInMb</span></span>
<span data-ttu-id="d1f61-151">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="d1f61-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1f61-152">-SubscriptionId</span></span>
<span data-ttu-id="d1f61-153">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f61-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d1f61-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1f61-154">-Tag</span></span>
<span data-ttu-id="d1f61-155">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="d1f61-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d1f61-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f61-156">-Confirm</span></span>
<span data-ttu-id="d1f61-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1f61-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f61-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f61-158">-WhatIf</span></span>
<span data-ttu-id="d1f61-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1f61-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f61-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1f61-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f61-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f61-161">CommonParameters</span></span>
<span data-ttu-id="d1f61-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f61-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f61-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1f61-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f61-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1f61-164">INPUTS</span></span>

### <span data-ttu-id="d1f61-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d1f61-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d1f61-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1f61-166">OUTPUTS</span></span>

### <span data-ttu-id="d1f61-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="d1f61-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="d1f61-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1f61-168">NOTES</span></span>

<span data-ttu-id="d1f61-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d1f61-169">ALIASES</span></span>

<span data-ttu-id="d1f61-170">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d1f61-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1f61-171">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d1f61-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1f61-172">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1f61-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1f61-173"><IMySqlIdentity>INPUTOBJECT: parametro identity.</span><span class="sxs-lookup"><span data-stu-id="d1f61-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="d1f61-174">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d1f61-175">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="d1f61-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d1f61-176">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d1f61-177">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d1f61-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1f61-178">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d1f61-179">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d1f61-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d1f61-180">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1f61-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d1f61-181">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d1f61-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="d1f61-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d1f61-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d1f61-183">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="d1f61-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d1f61-184">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1f61-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d1f61-185">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1f61-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d1f61-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1f61-186">RELATED LINKS</span></span>

