---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 95807621ffb054610a5778872db243eea50a7efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968910"
---
# <span data-ttu-id="a7bf8-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="a7bf8-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="a7bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bf8-103">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="a7bf8-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="a7bf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7bf8-104">SYNTAX</span></span>

### <span data-ttu-id="a7bf8-105">GeoRestore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7bf8-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7bf8-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="a7bf8-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a7bf8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7bf8-107">DESCRIPTION</span></span>
<span data-ttu-id="a7bf8-108">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="a7bf8-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="a7bf8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7bf8-109">EXAMPLES</span></span>

### <span data-ttu-id="a7bf8-110">Esempio 1: Ripristinare il server MySql con GeoReplica Restore</span><span class="sxs-lookup"><span data-stu-id="a7bf8-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="a7bf8-111">Questo cmdlet ripristina il server MySql tramite GeoReplica Restore.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="a7bf8-112">Esempio 2: Ripristinare il server MySql con PointInTime Restore</span><span class="sxs-lookup"><span data-stu-id="a7bf8-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="a7bf8-113">Questi cmdlet ripristinano il server MySql tramite PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="a7bf8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7bf8-114">PARAMETERS</span></span>

### <span data-ttu-id="a7bf8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7bf8-115">-AsJob</span></span>
<span data-ttu-id="a7bf8-116">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="a7bf8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bf8-117">-DefaultProfile</span></span>
<span data-ttu-id="a7bf8-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7bf8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7bf8-119">-InputObject</span></span>
<span data-ttu-id="a7bf8-120">Oggetto server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-120">The source server object to restore from.</span></span>
<span data-ttu-id="a7bf8-121">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7bf8-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a7bf8-122">-Location</span></span>
<span data-ttu-id="a7bf8-123">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="a7bf8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a7bf8-124">-Name</span></span>
<span data-ttu-id="a7bf8-125">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-125">The name of the server.</span></span>

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

### <span data-ttu-id="a7bf8-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7bf8-126">-NoWait</span></span>
<span data-ttu-id="a7bf8-127">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a7bf8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7bf8-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7bf8-129">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a7bf8-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="a7bf8-130">-RestorePointInTime</span></span>
<span data-ttu-id="a7bf8-131">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="a7bf8-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="a7bf8-132">-Sku</span></span>
<span data-ttu-id="a7bf8-133">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="a7bf8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7bf8-134">-SubscriptionId</span></span>
<span data-ttu-id="a7bf8-135">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a7bf8-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7bf8-136">-Tag</span></span>
<span data-ttu-id="a7bf8-137">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="a7bf8-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="a7bf8-138">-UseGeoRestore</span></span>
<span data-ttu-id="a7bf8-139">Usare la modalità geografica per ripristinare</span><span class="sxs-lookup"><span data-stu-id="a7bf8-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="a7bf8-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="a7bf8-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="a7bf8-141">Usare la modalità PointInTime per ripristinare</span><span class="sxs-lookup"><span data-stu-id="a7bf8-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="a7bf8-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7bf8-142">-Confirm</span></span>
<span data-ttu-id="a7bf8-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7bf8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7bf8-144">-WhatIf</span></span>
<span data-ttu-id="a7bf8-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7bf8-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7bf8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bf8-147">CommonParameters</span></span>
<span data-ttu-id="a7bf8-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bf8-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bf8-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7bf8-150">INPUTS</span></span>

### <span data-ttu-id="a7bf8-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a7bf8-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a7bf8-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7bf8-152">OUTPUTS</span></span>

### <span data-ttu-id="a7bf8-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a7bf8-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a7bf8-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7bf8-154">NOTES</span></span>

<span data-ttu-id="a7bf8-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a7bf8-155">ALIASES</span></span>

<span data-ttu-id="a7bf8-156">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a7bf8-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7bf8-157">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7bf8-158">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7bf8-159"><IServer>INPUTOBJECT: oggetto server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="a7bf8-160">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="a7bf8-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="a7bf8-161">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a7bf8-162">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a7bf8-163">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="a7bf8-164">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="a7bf8-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="a7bf8-165">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="a7bf8-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="a7bf8-166">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="a7bf8-167">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="a7bf8-168">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="a7bf8-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: stato che indica se la crittografia dell'infrastruttura abilitata per il server è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="a7bf8-170">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="a7bf8-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: consente di applicare una versione minima di Tls per il server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="a7bf8-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: indica se l'accesso alla rete pubblica è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="a7bf8-173">Il valore è facoltativo ma, se passato, deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="a7bf8-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="a7bf8-174">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="a7bf8-175">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="a7bf8-176">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="a7bf8-177">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="a7bf8-178">`[SkuName <String>]`: il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="a7bf8-179">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="a7bf8-180">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Base.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="a7bf8-181">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="a7bf8-182">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="a7bf8-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="a7bf8-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="a7bf8-185">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="a7bf8-186">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="a7bf8-187">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="a7bf8-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="a7bf8-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7bf8-188">RELATED LINKS</span></span>

