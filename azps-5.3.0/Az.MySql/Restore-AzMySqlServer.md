---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 7a53cefa9aca7e4ea679b31763c19e82d4d1e841
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475178"
---
# <span data-ttu-id="263e3-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="263e3-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="263e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="263e3-102">SYNOPSIS</span></span>
<span data-ttu-id="263e3-103">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="263e3-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="263e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="263e3-104">SYNTAX</span></span>

### <span data-ttu-id="263e3-105">Georestore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="263e3-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="263e3-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="263e3-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="263e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="263e3-107">DESCRIPTION</span></span>
<span data-ttu-id="263e3-108">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="263e3-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="263e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="263e3-109">EXAMPLES</span></span>

### <span data-ttu-id="263e3-110">Esempio 1: ripristinare il server MySql tramite il ripristino di georeplica</span><span class="sxs-lookup"><span data-stu-id="263e3-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="263e3-111">Questo cmdlet consente di ripristinare il server MySql usando il ripristino di georeplica.</span><span class="sxs-lookup"><span data-stu-id="263e3-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="263e3-112">Esempio 2: ripristinare il server MySql tramite il ripristino di PointInTime</span><span class="sxs-lookup"><span data-stu-id="263e3-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="263e3-113">Questi cmdlet ripristinano il server MySql usando PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="263e3-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="263e3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="263e3-114">PARAMETERS</span></span>

### <span data-ttu-id="263e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="263e3-115">-AsJob</span></span>
<span data-ttu-id="263e3-116">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="263e3-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="263e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263e3-117">-DefaultProfile</span></span>
<span data-ttu-id="263e3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="263e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="263e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="263e3-119">-InputObject</span></span>
<span data-ttu-id="263e3-120">Oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="263e3-120">The source server object to restore from.</span></span>
<span data-ttu-id="263e3-121">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="263e3-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="263e3-122">-Location</span></span>
<span data-ttu-id="263e3-123">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="263e3-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="263e3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="263e3-124">-Name</span></span>
<span data-ttu-id="263e3-125">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="263e3-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="263e3-126">-NoWait</span></span>
<span data-ttu-id="263e3-127">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="263e3-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="263e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="263e3-129">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="263e3-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="263e3-130">-RestorePointInTime</span></span>
<span data-ttu-id="263e3-131">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="263e3-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="263e3-132">-Sku</span></span>
<span data-ttu-id="263e3-133">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="263e3-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="263e3-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="263e3-134">-SubscriptionId</span></span>
<span data-ttu-id="263e3-135">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="263e3-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="263e3-136">-Tag</span></span>
<span data-ttu-id="263e3-137">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="263e3-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="263e3-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="263e3-138">-UseGeoRestore</span></span>
<span data-ttu-id="263e3-139">Usare la modalità Geo per ripristinare</span><span class="sxs-lookup"><span data-stu-id="263e3-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="263e3-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="263e3-141">Usare la modalità PointInTime per ripristinare</span><span class="sxs-lookup"><span data-stu-id="263e3-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263e3-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="263e3-142">-Confirm</span></span>
<span data-ttu-id="263e3-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="263e3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="263e3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="263e3-144">-WhatIf</span></span>
<span data-ttu-id="263e3-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="263e3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="263e3-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="263e3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="263e3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263e3-147">CommonParameters</span></span>
<span data-ttu-id="263e3-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263e3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263e3-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="263e3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263e3-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="263e3-150">INPUTS</span></span>

### <span data-ttu-id="263e3-151">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="263e3-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="263e3-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="263e3-152">OUTPUTS</span></span>

### <span data-ttu-id="263e3-153">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="263e3-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="263e3-154">Note</span><span class="sxs-lookup"><span data-stu-id="263e3-154">NOTES</span></span>

<span data-ttu-id="263e3-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="263e3-155">ALIASES</span></span>

<span data-ttu-id="263e3-156">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="263e3-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="263e3-157">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="263e3-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="263e3-158">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="263e3-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="263e3-159">INPUTOBJECT <IServer> : l'oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="263e3-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="263e3-160">`Location <String>`: La posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="263e3-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="263e3-161">`SkuName <String>`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="263e3-161">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="263e3-162">`[Tag <ITrackedResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="263e3-162">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="263e3-163">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="263e3-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="263e3-164">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="263e3-164">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="263e3-165">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="263e3-165">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="263e3-166">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="263e3-166">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="263e3-167">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="263e3-167">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="263e3-168">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="263e3-168">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="263e3-169">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="263e3-169">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="263e3-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stato che indica se il server ha abilitato la crittografia dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="263e3-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="263e3-171">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="263e3-171">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="263e3-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Applicare una versione TLS minima per il server.</span><span class="sxs-lookup"><span data-stu-id="263e3-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="263e3-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se l'accesso alla rete pubblica è consentito per il server.</span><span class="sxs-lookup"><span data-stu-id="263e3-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="263e3-174">Il valore è facoltativo ma, se passato, deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="263e3-174">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="263e3-175">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="263e3-175">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="263e3-176">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="263e3-176">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="263e3-177">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="263e3-177">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="263e3-178">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="263e3-178">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="263e3-179">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="263e3-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="263e3-180">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="263e3-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="263e3-181">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="263e3-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="263e3-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="263e3-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="263e3-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="263e3-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="263e3-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="263e3-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="263e3-185">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="263e3-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="263e3-186">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="263e3-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="263e3-187">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="263e3-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="263e3-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="263e3-188">RELATED LINKS</span></span>

