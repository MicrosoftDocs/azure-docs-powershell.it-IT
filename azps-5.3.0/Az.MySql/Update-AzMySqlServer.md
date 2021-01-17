---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: b205f3d4eb9b1ebce360596714ea2524fb2e3be2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475160"
---
# <span data-ttu-id="6008d-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="6008d-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="6008d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6008d-102">SYNOPSIS</span></span>
<span data-ttu-id="6008d-103">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="6008d-103">Updates an existing server.</span></span>
<span data-ttu-id="6008d-104">Il corpo della richiesta può contenere uno a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="6008d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6008d-105">USA invece Update-AzMySqlConfiguration se vuoi aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="6008d-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6008d-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6008d-106">SYNTAX</span></span>

### <span data-ttu-id="6008d-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6008d-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6008d-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6008d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6008d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6008d-109">DESCRIPTION</span></span>
<span data-ttu-id="6008d-110">Aggiorna un server esistente.</span><span class="sxs-lookup"><span data-stu-id="6008d-110">Updates an existing server.</span></span>
<span data-ttu-id="6008d-111">Il corpo della richiesta può contenere uno a molte delle proprietà presenti nella definizione del server normale.</span><span class="sxs-lookup"><span data-stu-id="6008d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6008d-112">USA invece Update-AzMySqlConfiguration se vuoi aggiornare i parametri del server, ad esempio wait_timeout o net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="6008d-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6008d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6008d-113">EXAMPLES</span></span>

### <span data-ttu-id="6008d-114">Esempio 1: aggiornare il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="6008d-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="6008d-115">Questo cmdlet aggiorna il server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="6008d-116">Esempio 2: aggiornare il server MySql per identità.</span><span class="sxs-lookup"><span data-stu-id="6008d-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="6008d-117">Questo cmdlet aggiorna il server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="6008d-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="6008d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6008d-118">PARAMETERS</span></span>

### <span data-ttu-id="6008d-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6008d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6008d-120">La password dell'account di accesso dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="6008d-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="6008d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6008d-121">-AsJob</span></span>
<span data-ttu-id="6008d-122">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="6008d-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="6008d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6008d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="6008d-124">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="6008d-124">Backup retention days for the server.</span></span>
<span data-ttu-id="6008d-125">Il numero di giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="6008d-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6008d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6008d-126">-DefaultProfile</span></span>
<span data-ttu-id="6008d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6008d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6008d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6008d-128">-InputObject</span></span>
<span data-ttu-id="6008d-129">Parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="6008d-129">Identity Parameter.</span></span>
<span data-ttu-id="6008d-130">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6008d-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6008d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6008d-131">-Name</span></span>
<span data-ttu-id="6008d-132">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-132">The name of the server.</span></span>

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

### <span data-ttu-id="6008d-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6008d-133">-NoWait</span></span>
<span data-ttu-id="6008d-134">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="6008d-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6008d-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="6008d-135">-ReplicationRole</span></span>
<span data-ttu-id="6008d-136">Ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="6008d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6008d-137">-ResourceGroupName</span></span>
<span data-ttu-id="6008d-138">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6008d-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6008d-139">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="6008d-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6008d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="6008d-140">-Sku</span></span>
<span data-ttu-id="6008d-141">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6008d-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6008d-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6008d-142">-SkuCapacity</span></span>
<span data-ttu-id="6008d-143">La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="6008d-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="6008d-144">-SkuFamily</span></span>
<span data-ttu-id="6008d-145">La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="6008d-145">The family of hardware.</span></span>

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

### <span data-ttu-id="6008d-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6008d-146">-SkuTier</span></span>
<span data-ttu-id="6008d-147">Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="6008d-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="6008d-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="6008d-148">-SslEnforcement</span></span>
<span data-ttu-id="6008d-149">Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="6008d-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="6008d-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="6008d-150">-StorageAutogrow</span></span>
<span data-ttu-id="6008d-151">Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6008d-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="6008d-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6008d-152">-StorageInMb</span></span>
<span data-ttu-id="6008d-153">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="6008d-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6008d-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6008d-154">-SubscriptionId</span></span>
<span data-ttu-id="6008d-155">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="6008d-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6008d-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="6008d-156">-Tag</span></span>
<span data-ttu-id="6008d-157">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="6008d-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6008d-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6008d-158">-Confirm</span></span>
<span data-ttu-id="6008d-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6008d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6008d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6008d-160">-WhatIf</span></span>
<span data-ttu-id="6008d-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6008d-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6008d-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6008d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6008d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6008d-163">CommonParameters</span></span>
<span data-ttu-id="6008d-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6008d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6008d-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6008d-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6008d-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6008d-166">INPUTS</span></span>

### <span data-ttu-id="6008d-167">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6008d-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6008d-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6008d-168">OUTPUTS</span></span>

### <span data-ttu-id="6008d-169">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="6008d-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6008d-170">Note</span><span class="sxs-lookup"><span data-stu-id="6008d-170">NOTES</span></span>

<span data-ttu-id="6008d-171">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6008d-171">ALIASES</span></span>

<span data-ttu-id="6008d-172">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6008d-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6008d-173">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6008d-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6008d-174">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6008d-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6008d-175">INPUTOBJECT <IMySqlIdentity> : parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="6008d-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="6008d-176">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6008d-177">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="6008d-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6008d-178">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6008d-179">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6008d-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6008d-180">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-180">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="6008d-181">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="6008d-181">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6008d-182">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6008d-182">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6008d-183">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6008d-183">The name is case insensitive.</span></span>
  - <span data-ttu-id="6008d-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6008d-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6008d-185">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="6008d-185">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6008d-186">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6008d-186">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6008d-187">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6008d-187">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6008d-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6008d-188">RELATED LINKS</span></span>

