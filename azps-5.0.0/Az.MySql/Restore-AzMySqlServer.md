---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200039"
---
# <span data-ttu-id="dd7a7-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="dd7a7-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="dd7a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7a7-103">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="dd7a7-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="dd7a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd7a7-104">SYNTAX</span></span>

### <span data-ttu-id="dd7a7-105">Georestore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd7a7-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd7a7-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="dd7a7-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dd7a7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd7a7-107">DESCRIPTION</span></span>
<span data-ttu-id="dd7a7-108">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="dd7a7-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="dd7a7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd7a7-109">EXAMPLES</span></span>

### <span data-ttu-id="dd7a7-110">Esempio 1: ripristinare il server MySql tramite il ripristino di georeplica</span><span class="sxs-lookup"><span data-stu-id="dd7a7-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="dd7a7-111">Questo cmdlet consente di ripristinare il server MySql usando il ripristino di georeplica.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="dd7a7-112">Esempio 2: ripristinare il server MySql tramite il ripristino di PointInTime</span><span class="sxs-lookup"><span data-stu-id="dd7a7-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="dd7a7-113">Questi cmdlet ripristinano il server MySql usando PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="dd7a7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd7a7-114">PARAMETERS</span></span>

### <span data-ttu-id="dd7a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd7a7-115">-AsJob</span></span>
<span data-ttu-id="dd7a7-116">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="dd7a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7a7-117">-DefaultProfile</span></span>
<span data-ttu-id="dd7a7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd7a7-119">-InputObject</span></span>
<span data-ttu-id="dd7a7-120">Oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-120">The source server object to restore from.</span></span>
<span data-ttu-id="dd7a7-121">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dd7a7-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dd7a7-122">-Location</span></span>
<span data-ttu-id="dd7a7-123">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="dd7a7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd7a7-124">-Name</span></span>
<span data-ttu-id="dd7a7-125">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-125">The name of the server.</span></span>

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

### <span data-ttu-id="dd7a7-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="dd7a7-126">-NoWait</span></span>
<span data-ttu-id="dd7a7-127">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="dd7a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd7a7-129">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dd7a7-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="dd7a7-130">-RestorePointInTime</span></span>
<span data-ttu-id="dd7a7-131">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="dd7a7-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="dd7a7-132">-Sku</span></span>
<span data-ttu-id="dd7a7-133">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="dd7a7-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd7a7-134">-SubscriptionId</span></span>
<span data-ttu-id="dd7a7-135">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="dd7a7-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd7a7-136">-Tag</span></span>
<span data-ttu-id="dd7a7-137">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="dd7a7-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="dd7a7-138">-UseGeoRestore</span></span>
<span data-ttu-id="dd7a7-139">Usare la modalità Geo per ripristinare</span><span class="sxs-lookup"><span data-stu-id="dd7a7-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="dd7a7-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="dd7a7-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="dd7a7-141">Usare la modalità PointInTime per ripristinare</span><span class="sxs-lookup"><span data-stu-id="dd7a7-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="dd7a7-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd7a7-142">-Confirm</span></span>
<span data-ttu-id="dd7a7-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd7a7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd7a7-144">-WhatIf</span></span>
<span data-ttu-id="dd7a7-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd7a7-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd7a7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7a7-147">CommonParameters</span></span>
<span data-ttu-id="dd7a7-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7a7-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd7a7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7a7-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd7a7-150">INPUTS</span></span>

### <span data-ttu-id="dd7a7-151">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="dd7a7-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="dd7a7-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd7a7-152">OUTPUTS</span></span>

### <span data-ttu-id="dd7a7-153">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="dd7a7-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="dd7a7-154">Note</span><span class="sxs-lookup"><span data-stu-id="dd7a7-154">NOTES</span></span>

<span data-ttu-id="dd7a7-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dd7a7-155">ALIASES</span></span>

<span data-ttu-id="dd7a7-156">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd7a7-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd7a7-157">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd7a7-158">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd7a7-159">INPUTOBJECT <IServer> : l'oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="dd7a7-160">`Location <String>`: La posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="dd7a7-161">`[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="dd7a7-162">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dd7a7-163">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="dd7a7-164">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="dd7a7-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="dd7a7-165">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="dd7a7-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="dd7a7-166">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="dd7a7-167">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="dd7a7-168">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="dd7a7-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stato che indica se il server ha abilitato la crittografia dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="dd7a7-170">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="dd7a7-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Applicare una versione TLS minima per il server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="dd7a7-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se l'accesso alla rete pubblica è consentito per il server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="dd7a7-173">Il valore è facoltativo ma, se passato, deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="dd7a7-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="dd7a7-174">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="dd7a7-175">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="dd7a7-176">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="dd7a7-177">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="dd7a7-178">`[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="dd7a7-179">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="dd7a7-180">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="dd7a7-181">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="dd7a7-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="dd7a7-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="dd7a7-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="dd7a7-185">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="dd7a7-186">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="dd7a7-187">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="dd7a7-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="dd7a7-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd7a7-188">RELATED LINKS</span></span>
