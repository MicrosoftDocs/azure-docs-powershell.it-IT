---
title: Guida alla migrazione per Az 3.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell quando è stata rilasciata la versione 3.0 del modulo Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: 06be35bc3573d00d90a8cf2d822ac051ab72f6bb
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566493"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="38222-103">Guida alla migrazione per Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="38222-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="38222-104">Questo documento descrive le modifiche apportate tra le versioni 2.0.0 e 3.0.0 del modulo Az</span><span class="sxs-lookup"><span data-stu-id="38222-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="38222-105">Guida alla migrazione per Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="38222-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="38222-106">Batch</span><span class="sxs-lookup"><span data-stu-id="38222-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="38222-107">Incompatibilità con le versioni precedenti di `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="38222-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="38222-108">Calcolo</span><span class="sxs-lookup"><span data-stu-id="38222-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="38222-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="38222-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="38222-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="38222-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="38222-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="38222-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="38222-112">Risorse</span><span class="sxs-lookup"><span data-stu-id="38222-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="38222-113">Incompatibilità con le versioni precedenti di `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="38222-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="38222-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="38222-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="38222-115">Sql</span><span class="sxs-lookup"><span data-stu-id="38222-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="38222-116">Batch</span><span class="sxs-lookup"><span data-stu-id="38222-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="38222-117">Rimozione di `Get-AzBatchNodeAgentSku` e sostituzione con `Get-AzBatchSupportedImage`.</span><span class="sxs-lookup"><span data-stu-id="38222-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="38222-118">`Get-AzBatchSupportedImage` restituisce gli stessi dati di `Get-AzBatchNodeAgentSku` ma in un formato più descrittivo.</span><span class="sxs-lookup"><span data-stu-id="38222-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="38222-119">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="38222-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="38222-120">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="38222-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-121">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="38222-122">After</span><span class="sxs-lookup"><span data-stu-id="38222-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="38222-123">Incompatibilità delle versioni precedenti con il modulo Az.Resources</span><span class="sxs-lookup"><span data-stu-id="38222-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="38222-124">La versione 2.0.1 del modulo 'Az.Batch' è incompatibile con le versioni precedenti (1.7.0 o precedente) del modulo 'Az.Resources'.</span><span class="sxs-lookup"><span data-stu-id="38222-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="38222-125">Di conseguenza, non è possibile importare la versione 1.7.0 del modulo 'Az.Resources' quando viene importata la versione 2.0.1 del modulo 'Az.Batch'.</span><span class="sxs-lookup"><span data-stu-id="38222-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="38222-126">Per risolvere questo problema, è sufficiente aggiornare il modulo 'Az.Resources' alla versione 1.7.1 o successiva oppure installare semplicemente la versione più recente del modulo 'Az'.</span><span class="sxs-lookup"><span data-stu-id="38222-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="38222-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="38222-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="38222-128">Il parametro `UploadSizeInBytes` viene usato al posto di `DiskSizeGB` per `New-AzDiskConfig` quando CreateOption è Upload</span><span class="sxs-lookup"><span data-stu-id="38222-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="38222-129">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="38222-130">After</span><span class="sxs-lookup"><span data-stu-id="38222-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="38222-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="38222-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="38222-132">Il cmdlet `Get-AzHDInsightJobOutput` è stato aggiornato e ora supporta l'accesso granulare in base al ruolo alla chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="38222-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="38222-133">Gli utenti con ruolo di collaboratore, proprietario oppure operatore cluster HDInsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="38222-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="38222-134">Solo gli utenti con ruolo di lettore devono specificare il parametro `DefaultStorageAccountKey` in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="38222-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-135">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="38222-136">After</span><span class="sxs-lookup"><span data-stu-id="38222-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="38222-137">Il cmdlet `Add-AzHDInsightConfigValue` ha rimosso l'alias di `Add-AzHDInsightConfigValues`.</span><span class="sxs-lookup"><span data-stu-id="38222-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-138">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-138">Before</span></span>
<span data-ttu-id="38222-139">Uso di funzionalità deprecate</span><span class="sxs-lookup"><span data-stu-id="38222-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="38222-140">After</span><span class="sxs-lookup"><span data-stu-id="38222-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="38222-141">È stato aggiunto un nuovo cmdlet `Disable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="38222-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="38222-142">Usare questo cmdlet per disabilitare il monitoraggio in un cluster HDInsight (sostituisce `Disable-AzHDInsightOperationsManagementSuite` e `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="38222-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="38222-143">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="38222-144">After</span><span class="sxs-lookup"><span data-stu-id="38222-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="38222-145">È stato aggiunto un nuovo cmdlet `Enable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="38222-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="38222-146">Usare questo cmdlet per abilitare il monitoraggio in un cluster HDInsight (sostituisce `Enable-AzHDInsightOperationsManagementSuite` e `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="38222-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="38222-147">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="38222-148">After</span><span class="sxs-lookup"><span data-stu-id="38222-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="38222-149">È stato aggiunto un nuovo cmdlet `Get-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="38222-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="38222-150">Usare questo cmdlet per ottenere lo stato dell'installazione del monitoraggio in un cluster di Azure HDInsight (sostituisce `Get-AzHDInsightOperationsManagementSuite` e `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="38222-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="38222-151">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="38222-152">After</span><span class="sxs-lookup"><span data-stu-id="38222-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="38222-153">Il cmdlet `Get-HDInsightProperty` ha rimosso l'alias di `Get-AzHDInsightProperties`.</span><span class="sxs-lookup"><span data-stu-id="38222-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-154">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-154">Before</span></span>
<span data-ttu-id="38222-155">Uso di funzionalità deprecate</span><span class="sxs-lookup"><span data-stu-id="38222-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="38222-156">After</span><span class="sxs-lookup"><span data-stu-id="38222-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="38222-157">Sono stati rimossi i cmdlet `Grant-AzHDInsightRdpServicesAccess` e `Revoke-AzHDInsightRdpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="38222-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="38222-158">Non sono più necessari perché i cluster che usano un tipo sistema operativo Windows non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="38222-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="38222-159">Creare invece un cluster usando un tipo di sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="38222-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="38222-160">Il tipo di output di `Remove-AzHDInsightCluster` è cambiato da `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` a `bool`.</span><span class="sxs-lookup"><span data-stu-id="38222-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-161">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="38222-162">After</span><span class="sxs-lookup"><span data-stu-id="38222-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="38222-163">Il cmdlet è deprecato.</span><span class="sxs-lookup"><span data-stu-id="38222-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="38222-164">Non sono disponibili sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="38222-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="38222-165">Il tipo di output di `Set-AzHDInsightGatewayCredential` è cambiato da `HttpConnectivitySettings` a `AzureHDInsightGatewaySettings`.</span><span class="sxs-lookup"><span data-stu-id="38222-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="38222-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="38222-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="38222-167">Questo alias è stato rimosso, usare `New-AzIotHubImportDevice` in alternativa.</span><span class="sxs-lookup"><span data-stu-id="38222-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-168">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="38222-169">After</span><span class="sxs-lookup"><span data-stu-id="38222-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="38222-170">Questo alias è stato rimosso, usare `New-AzIotHubExportDevice` in alternativa.</span><span class="sxs-lookup"><span data-stu-id="38222-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-171">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="38222-172">After</span><span class="sxs-lookup"><span data-stu-id="38222-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="38222-173">Il parametro `EventHubEndPointName` è deprecato e non è stato sostituito, perché l'hub IoT include un unico endpoint predefinito ("events") in grado di gestire messaggi di sistemi e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="38222-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-174">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="38222-175">After</span><span class="sxs-lookup"><span data-stu-id="38222-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="38222-176">Il parametro `EventHubEndPointName` è deprecato e non è stato sostituito, perché l'hub IoT include un unico endpoint predefinito ("events") in grado di gestire messaggi di sistemi e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="38222-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-177">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="38222-178">After</span><span class="sxs-lookup"><span data-stu-id="38222-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="38222-179">Il parametro `EventHubEndPointName` è deprecato e non è stato sostituito, perché l'hub IoT include un unico endpoint predefinito ("events") in grado di gestire messaggi di sistemi e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="38222-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-180">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="38222-181">After</span><span class="sxs-lookup"><span data-stu-id="38222-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="38222-182">Il parametro `OperationsMonitoringProperties` è deprecato e non è stato sostituito perché l'hub IoT non usa più l'endpoint predefinito ("operationsMonitoringEvents").</span><span class="sxs-lookup"><span data-stu-id="38222-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="38222-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="38222-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="38222-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` e `ASRRecoveryPlanGroup.EndGroupActions` sono stati rimossi dall'output.</span><span class="sxs-lookup"><span data-stu-id="38222-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="38222-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` e `ASRRecoveryPlanGroup.EndGroupActions` sono stati rimossi dall'output.</span><span class="sxs-lookup"><span data-stu-id="38222-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="38222-186">Il parametro IncludeDiskId è stato cambiato per supportare la scrittura diretta in un disco gestito in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="38222-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-187">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="38222-188">After</span><span class="sxs-lookup"><span data-stu-id="38222-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="38222-189">Risorse</span><span class="sxs-lookup"><span data-stu-id="38222-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="38222-190">Incompatibilità della versione precedente con il modulo Az.Batch</span><span class="sxs-lookup"><span data-stu-id="38222-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="38222-191">La versione 1.7.1 del modulo 'Az.Resources' è incompatibile con le versioni precedenti (1.1.2 o precedente) del modulo 'Az.Batch'.</span><span class="sxs-lookup"><span data-stu-id="38222-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="38222-192">Di conseguenza, non è possibile importare la versione 1.1.2 del modulo 'Az.Batch' quando viene importata la versione 1.7.1 del modulo 'Az.Resources'.</span><span class="sxs-lookup"><span data-stu-id="38222-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="38222-193">Per risolvere questo problema, è sufficiente aggiornare il modulo 'Az.Batch' alla versione 2.0.1 o successiva oppure installare semplicemente la versione più recente del modulo 'Az'.</span><span class="sxs-lookup"><span data-stu-id="38222-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="38222-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="38222-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="38222-195">`Add-ServiceFabricApplicationCertificate` è stato rimosso perché questo scenario è gestito da `Add-AzVmssSecret`.</span><span class="sxs-lookup"><span data-stu-id="38222-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-196">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="38222-197">After</span><span class="sxs-lookup"><span data-stu-id="38222-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="38222-198">Sql</span><span class="sxs-lookup"><span data-stu-id="38222-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="38222-199">Si noti che la connessione sicura è deprecata e quindi il comando è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="38222-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="38222-200">Usare il pannello del database SQL nel portale di Azure per visualizzare le stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="38222-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="38222-201">L'alias `Get-AzSqlDatabaseIndexRecommendations` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="38222-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="38222-202">Usare invece `Get-AzSqlDatabaseIndexRecommendation`.</span><span class="sxs-lookup"><span data-stu-id="38222-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="38222-203">L'alias `Get-AzSqlDatabaseRestorePoints` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="38222-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="38222-204">Usare invece `Get-AzSqlDatabaseRestorePoint`.</span><span class="sxs-lookup"><span data-stu-id="38222-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="38222-205">Il cmdlet `Get-AzSqlDatabaseAudit` sostituisce questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38222-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="38222-206">Il tipo di output è cambiato dal tipo :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' esistente al nuovo tipo :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', rimuovendo le proprietà `AuditState` e `StorageAccountName`.</span><span class="sxs-lookup"><span data-stu-id="38222-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="38222-207">e `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="38222-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="38222-208">Gli script possono recuperare le informazioni sull'account di archiviazione dalla nuova proprietà `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="38222-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-209">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="38222-210">After</span><span class="sxs-lookup"><span data-stu-id="38222-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="38222-211">Il cmdlet `Set-AzSqlDatabaseAudit` sostituisce questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38222-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="38222-212">Il tipo di output è cambiato dal tipo :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' esistente al nuovo tipo :'bool'</span><span class="sxs-lookup"><span data-stu-id="38222-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="38222-213">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-214">After</span><span class="sxs-lookup"><span data-stu-id="38222-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="38222-215">Il cmdlet `Get-AzSqlServerAudit` sostituisce questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38222-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="38222-216">Il tipo di output è cambiato dal tipo :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' esistente al nuovo tipo :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span><span class="sxs-lookup"><span data-stu-id="38222-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="38222-217">Le proprietà `AuditState`, `StorageAccountName`e `StorageAccountSubscriptionId` sono state rimosse.</span><span class="sxs-lookup"><span data-stu-id="38222-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="38222-218">Gli script che usano le proprietà `StorageAccountName` e `StorageAccountSubscriptionId` possono recuperare queste informazioni dalla nuova proprietà `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="38222-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="38222-219">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="38222-220">After</span><span class="sxs-lookup"><span data-stu-id="38222-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="38222-221">Il cmdlet `Set-AzSqlServerAudit` sostituisce questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38222-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="38222-222">Il tipo di output è cambiato dal tipo :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' esistente al nuovo tipo :'bool'</span><span class="sxs-lookup"><span data-stu-id="38222-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="38222-223">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="38222-224">After</span><span class="sxs-lookup"><span data-stu-id="38222-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="38222-225">Il cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` è stato sostituito da `Get-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-226">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="38222-227">After</span><span class="sxs-lookup"><span data-stu-id="38222-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="38222-228">Il cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` è stato sostituito da `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-229">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="38222-230">After</span><span class="sxs-lookup"><span data-stu-id="38222-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="38222-231">Il cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` è stato sostituito da `Update-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-232">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="38222-233">After</span><span class="sxs-lookup"><span data-stu-id="38222-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="38222-234">Il cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` è stato sostituito da `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-235">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-236">After</span><span class="sxs-lookup"><span data-stu-id="38222-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="38222-237">Il cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` è stato sostituito da `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-238">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="38222-239">After</span><span class="sxs-lookup"><span data-stu-id="38222-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="38222-240">Il cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` è stato sostituito da `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-241">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-242">After</span><span class="sxs-lookup"><span data-stu-id="38222-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-243">Il cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` è stato sostituito da `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-244">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="38222-245">After</span><span class="sxs-lookup"><span data-stu-id="38222-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-246">Il cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` è stato sostituito da `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-247">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-248">After</span><span class="sxs-lookup"><span data-stu-id="38222-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-249">Il cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` è stato sostituito da `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-250">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-251">After</span><span class="sxs-lookup"><span data-stu-id="38222-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-252">Il cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` è stato sostituito da `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-253">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="38222-254">After</span><span class="sxs-lookup"><span data-stu-id="38222-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-255">Il cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` è stato sostituito da `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-256">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-257">After</span><span class="sxs-lookup"><span data-stu-id="38222-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-258">Il cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` è stato sostituito da `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-259">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-260">After</span><span class="sxs-lookup"><span data-stu-id="38222-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-261">Il cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` è stato sostituito da `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-262">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="38222-263">After</span><span class="sxs-lookup"><span data-stu-id="38222-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-264">Il cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` è stato sostituito da `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-265">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-266">After</span><span class="sxs-lookup"><span data-stu-id="38222-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-267">Il cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` è stato sostituito da `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-268">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-269">After</span><span class="sxs-lookup"><span data-stu-id="38222-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-270">Il cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` è stato sostituito da `Update-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-271">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="38222-272">After</span><span class="sxs-lookup"><span data-stu-id="38222-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-273">Il cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` è stato sostituito da `Get-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-274">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-275">After</span><span class="sxs-lookup"><span data-stu-id="38222-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="38222-276">Il cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` è stato sostituito da `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-277">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-278">After</span><span class="sxs-lookup"><span data-stu-id="38222-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="38222-279">Il cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` è stato eliminato e non viene sostituito</span><span class="sxs-lookup"><span data-stu-id="38222-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="38222-280">Il cmdlet `Get-AzSqlServerThreatDetectionPolicy` è stato sostituito da `Get-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-281">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="38222-282">After</span><span class="sxs-lookup"><span data-stu-id="38222-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="38222-283">Il cmdlet `Remove-AzSqlServerThreatDetectionPolicy` è stato sostituito da `Clear-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-284">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="38222-285">After</span><span class="sxs-lookup"><span data-stu-id="38222-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="38222-286">Il cmdlet `Set-AzSqlServerThreatDetectionPolicy` è stato sostituito da `Update-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-287">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="38222-288">After</span><span class="sxs-lookup"><span data-stu-id="38222-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="38222-289">Il cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` è stato sostituito da `Get-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-290">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="38222-291">After</span><span class="sxs-lookup"><span data-stu-id="38222-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="38222-292">Il cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` è stato sostituito da `Update-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-293">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="38222-294">After</span><span class="sxs-lookup"><span data-stu-id="38222-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="38222-295">Il cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` è stato sostituito da `Clear-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="38222-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="38222-296">Prima</span><span class="sxs-lookup"><span data-stu-id="38222-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="38222-297">After</span><span class="sxs-lookup"><span data-stu-id="38222-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
