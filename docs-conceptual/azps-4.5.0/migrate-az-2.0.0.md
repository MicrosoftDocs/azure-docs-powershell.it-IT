---
title: Guida alla migrazione per Az 2.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell quando è stata rilasciata la versione 2.0 del modulo Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 91362f3cc6b35e96a543c1304fb55acbf373d291
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566529"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="1b2d9-103">Guida alla migrazione per Az 2.0.0</span><span class="sxs-lookup"><span data-stu-id="1b2d9-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="1b2d9-104">Questo documento descrive le modifiche apportate tra le versioni 1.0.0 e 2.0.0 di Az.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="1b2d9-105">Sommario</span><span class="sxs-lookup"><span data-stu-id="1b2d9-105">Table of Contents</span></span>
- [<span data-ttu-id="1b2d9-106">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="1b2d9-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="1b2d9-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b2d9-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="1b2d9-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b2d9-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="1b2d9-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b2d9-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="1b2d9-110">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="1b2d9-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="1b2d9-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1b2d9-111">Az.Compute</span></span>

- <span data-ttu-id="1b2d9-112">Il parametro `Managed` è stato rimosso da `New-AzAvailabilitySet` e `Update-AzAvailabilitySet` ed è stato sostituito da ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="1b2d9-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-113">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-114">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="1b2d9-115">Per coerenza, il parametro `Image` è stato rimosso dai set di parametri 'ByName' e 'ByResourceId' in `Update-AzImage`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-116">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-116">Before</span></span>

  <span data-ttu-id="1b2d9-117">Si noti che il codice seguente è funzionante, ma il parametro ImageName passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-118">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="1b2d9-119">Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Restart-AzVM`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-120">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-120">Before</span></span>

  <span data-ttu-id="1b2d9-121">Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-122">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="1b2d9-123">Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Start-AzVM`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-124">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-124">Before</span></span>

  <span data-ttu-id="1b2d9-125">Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-126">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="1b2d9-127">Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Stop-AzVM`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-128">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-128">Before</span></span>

  <span data-ttu-id="1b2d9-129">Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-130">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="1b2d9-131">Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Remove-AzVM`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-132">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-132">Before</span></span>

  <span data-ttu-id="1b2d9-133">Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-134">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="1b2d9-135">Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Set-AzVM`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-136">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-136">Before</span></span>

  <span data-ttu-id="1b2d9-137">Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-138">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="1b2d9-139">Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Save-AzVMImage`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="1b2d9-140">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-140">Before</span></span>
  <span data-ttu-id="1b2d9-141">Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="1b2d9-142">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="1b2d9-143">È stata aggiunta la proprietà ProtectionPolicy per incapsulare la proprietà `ProtectFromScaleIn` in `PSVirtualMachineScaleSetVM`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-144">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-145">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="1b2d9-146">È stata aggiunta la proprietà ```EncryptionSettingsCollection``` per racchiudere `EncryptionSettings` in `PSDisk`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-147">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-148">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="1b2d9-149">È stata aggiunta la proprietà ```EncryptionSettingsCollection``` per racchiudere `EncryptionSettings` in `PSSnapshot`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-150">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-151">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="1b2d9-152">È stata rimossa la proprietà `VirtualMachineProfile` da `PSVirtualMachineScaleSet`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-153">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-154">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="1b2d9-155">Il cmdlet `Set-AzVMBootDiagnostic` ha rimosso l'alias di `Set-AzVMBootDiagnostics`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-156">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-156">Before</span></span>

  <span data-ttu-id="1b2d9-157">Uso di funzionalità deprecate</span><span class="sxs-lookup"><span data-stu-id="1b2d9-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-158">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="1b2d9-159">Il cmdlet `Export-AzLogAnalyticThrottledRequest` ha rimosso l'alias di `Export-AzLogAnalyticThrottledRequests`</span><span class="sxs-lookup"><span data-stu-id="1b2d9-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-160">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-160">Before</span></span>

  <span data-ttu-id="1b2d9-161">Uso di funzionalità deprecate</span><span class="sxs-lookup"><span data-stu-id="1b2d9-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-162">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="1b2d9-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b2d9-163">Az.HDInsight</span></span>

- <span data-ttu-id="1b2d9-164">Sono stati rimossi i cmdlet `Grant-AzHDInsightHttpServicesAccess` e `Revoke-AzHDInsightHttpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="1b2d9-165">Tali cmdlet non sono più necessari perché l'accesso HTTP è sempre abilitato in tutti i cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="1b2d9-166">È stato aggiunto un nuovo cmdlet `Set-AzHDInsightGatewayCredential`.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="1b2d9-167">Usare questo cmdlet per modificare nome utente e password HTTP del gateway (sostituisce `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="1b2d9-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="1b2d9-168">Il cmdlet `Get-AzHDInsightJobOutput` è stato aggiornato e ora supporta l'accesso granulare in base al ruolo alla chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="1b2d9-169">Gli utenti con ruolo di collaboratore, proprietario oppure operatore cluster HDInsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="1b2d9-170">Solo gli utenti con ruolo di lettore devono specificare il parametro `DefaultStorageAccountKey` in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="1b2d9-171">Per altre informazioni sulle modifiche degli accessi in base al ruolo, vedere [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update).</span><span class="sxs-lookup"><span data-stu-id="1b2d9-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="1b2d9-172">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-173">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="1b2d9-174">Solo gli utenti con ruolo di lettore per il cmdlet Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="1b2d9-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="1b2d9-175">Prima</span><span class="sxs-lookup"><span data-stu-id="1b2d9-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="1b2d9-176">After</span><span class="sxs-lookup"><span data-stu-id="1b2d9-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="1b2d9-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1b2d9-177">Az.Storage</span></span>

- <span data-ttu-id="1b2d9-178">Lo spazio dei nomi per i tipi restituiti dai cmdlet di BLOB, coda e file è stato modificato da `Microsoft.WindowsAzure.Storage` a `Microsoft.Azure.Storage`.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="1b2d9-179">Anche se non si tratta tecnicamente di una modifica di rilievo in base ai criteri per le modifiche di rilievo, può richiedere alcune modifiche nel codice che usa i metodi dell'SDK .NET di archiviazione per interagire con gli oggetti restituiti da tali cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="1b2d9-180">Esempio 1:  Aggiungere un messaggio a una coda (modificare lo spazio dei nomi dell'oggetto CloudQueueMessage)</span><span class="sxs-lookup"><span data-stu-id="1b2d9-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="1b2d9-181">Prima di:</span><span class="sxs-lookup"><span data-stu-id="1b2d9-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="1b2d9-182">Dopo:</span><span class="sxs-lookup"><span data-stu-id="1b2d9-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="1b2d9-183">Esempio 2:  Recuperare gli attributi di BLOB/File con AccessCondition (modificare lo spazio dei nomi dell'oggetto AccessCondition)</span><span class="sxs-lookup"><span data-stu-id="1b2d9-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="1b2d9-184">Prima di:</span><span class="sxs-lookup"><span data-stu-id="1b2d9-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="1b2d9-185">Dopo:</span><span class="sxs-lookup"><span data-stu-id="1b2d9-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="1b2d9-186">Anche se non si tratta tecnicamente di una modifica di rilievo, è possibile notare che le differenze nell'output della proprietà Sku.Name degli account di archiviazione restituiti dopo le modifiche apportate a `New/Get/Set-AzStorageAccount` sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="1b2d9-187">Dopo la modifica gli oggetti SkuName di input e di output sono allineati.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="1b2d9-188">"StandardLRS" -> "Standard_LRS";</span><span class="sxs-lookup"><span data-stu-id="1b2d9-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="1b2d9-189">"StandardGRS" -> "Standard_GRS";</span><span class="sxs-lookup"><span data-stu-id="1b2d9-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="1b2d9-190">"StandardRAGRS" -> "Standard_RAGRS";</span><span class="sxs-lookup"><span data-stu-id="1b2d9-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="1b2d9-191">"StandardZRS" -> "Standard_ZRS";</span><span class="sxs-lookup"><span data-stu-id="1b2d9-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="1b2d9-192">"PremiumLRS" -> "Premium_LRS";</span><span class="sxs-lookup"><span data-stu-id="1b2d9-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="1b2d9-193">Il comportamento predefinito del servizio quando si crea un account di archiviazione senza specificare l'argomento Kind è cambiato.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="1b2d9-194">Nelle versioni precedenti, quando si creava un account di archiviazione senza specificare l'argomento `Kind`, come valore di Kind per l'account di archiviazione si usava `Storage`. Nella nuova versione il valore predefinito di `Kind` è `StorageV2`.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="1b2d9-195">Per creare un account di archiviazione V1 in cui Kind è impostato su 'Storage', aggiungere il parametro '-Kind Storage'.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="1b2d9-196">Esempio: Creare un account di archiviazione (modifica dell'impostazione predefinita di Kind)</span><span class="sxs-lookup"><span data-stu-id="1b2d9-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="1b2d9-197">Prima di:</span><span class="sxs-lookup"><span data-stu-id="1b2d9-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="1b2d9-198">Dopo:</span><span class="sxs-lookup"><span data-stu-id="1b2d9-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
