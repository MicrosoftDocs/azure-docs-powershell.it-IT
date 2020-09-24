---
title: Guida alla migrazione per Az 2.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell quando è stata rilasciata la versione 2.0 del modulo Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2d8a3c04388bfc5028811f6d1b6caf2c6fce4147
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928170"
---
# <a name="migration-guide-for-az-200"></a>Guida alla migrazione per Az 2.0.0

Questo documento descrive le modifiche apportate tra le versioni 1.0.0 e 2.0.0 di Az. 

## <a name="table-of-contents"></a>Sommario
- [Modifiche che causano un'interruzione dei moduli](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Modifiche che causano un'interruzione dei moduli

### <a name="azcompute"></a>Az.Compute

- Il parametro `Managed` è stato rimosso da `New-AzAvailabilitySet` e `Update-AzAvailabilitySet` ed è stato sostituito da ```Sku = Aligned```

  #### <a name="before"></a>Prima

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- Per coerenza, il parametro `Image` è stato rimosso dai set di parametri 'ByName' e 'ByResourceId' in `Update-AzImage` 
  
  #### <a name="before"></a>Prima

  Si noti che il codice seguente è funzionante, ma il parametro ImageName passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Restart-AzVM`
  
  #### <a name="before"></a>Prima

  Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Start-AzVM`
  
  #### <a name="before"></a>Prima

  Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Stop-AzVM`
  
  #### <a name="before"></a>Prima

  Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Remove-AzVM`
  
  #### <a name="before"></a>Prima

  Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>After

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Set-AzVM`
  
  #### <a name="before"></a>Prima

  Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- Per coerenza, il parametro `Name` è stato rimosso dai set di parametri 'ByObject' e 'ByResourceId' in `Save-AzVMImage` 
  
  #### <a name="before"></a>Prima
  Si noti che il codice seguente è funzionante, ma il parametro Name passato non viene usato, di conseguenza la rimozione di questo parametro non influisce sul funzionamento.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>After
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- È stata aggiunta la proprietà ProtectionPolicy per incapsulare la proprietà `ProtectFromScaleIn` in `PSVirtualMachineScaleSetVM`

  #### <a name="before"></a>Prima

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- È stata aggiunta la proprietà ```EncryptionSettingsCollection``` per racchiudere `EncryptionSettings` in `PSDisk`

  #### <a name="before"></a>Prima

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

  #### <a name="after"></a>After

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

- È stata aggiunta la proprietà ```EncryptionSettingsCollection``` per racchiudere `EncryptionSettings` in `PSSnapshot`

  #### <a name="before"></a>Prima

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

  #### <a name="after"></a>After

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

- È stata rimossa la proprietà `VirtualMachineProfile` da `PSVirtualMachineScaleSet`

  #### <a name="before"></a>Prima

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- Il cmdlet `Set-AzVMBootDiagnostic` ha rimosso l'alias di `Set-AzVMBootDiagnostics`

  #### <a name="before"></a>Prima

  Uso di funzionalità deprecate

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- Il cmdlet `Export-AzLogAnalyticThrottledRequest` ha rimosso l'alias di `Export-AzLogAnalyticThrottledRequests`

  #### <a name="before"></a>Prima

  Uso di funzionalità deprecate

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>After

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- Sono stati rimossi i cmdlet `Grant-AzHDInsightHttpServicesAccess` e `Revoke-AzHDInsightHttpServicesAccess`. Tali cmdlet non sono più necessari perché l'accesso HTTP è sempre abilitato in tutti i cluster HDInsight.
- È stato aggiunto un nuovo cmdlet `Set-AzHDInsightGatewayCredential`. Usare questo cmdlet per modificare nome utente e password HTTP del gateway (sostituisce `Grant-AzHDInsightHttpServicesAccess`).
- Il cmdlet `Get-AzHDInsightJobOutput` è stato aggiornato e ora supporta l'accesso granulare in base al ruolo alla chiave di archiviazione.
    - Gli utenti con ruolo di collaboratore, proprietario oppure operatore cluster HDInsight non sono interessati.
    - Solo gli utenti con ruolo di lettore devono specificare il parametro `DefaultStorageAccountKey` in modo esplicito.

Per altre informazioni sulle modifiche degli accessi in base al ruolo, vedere [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update).

  #### <a name="before"></a>Prima

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Solo gli utenti con ruolo di lettore per il cmdlet Get-AzHDInsightJobOutput

  ####  <a name="before"></a>Prima

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>After

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Lo spazio dei nomi per i tipi restituiti dai cmdlet di BLOB, coda e file è stato modificato da `Microsoft.WindowsAzure.Storage` a `Microsoft.Azure.Storage`.  Anche se non si tratta tecnicamente di una modifica di rilievo in base ai criteri per le modifiche di rilievo, può richiedere alcune modifiche nel codice che usa i metodi dell'SDK .NET di archiviazione per interagire con gli oggetti restituiti da tali cmdlet.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Esempio 1:  Aggiungere un messaggio a una coda (modificare lo spazio dei nomi dell'oggetto CloudQueueMessage)

  Prima di: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Dopo:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Esempio 2:  Recuperare gli attributi di BLOB/File con AccessCondition (modificare lo spazio dei nomi dell'oggetto AccessCondition)

  Prima di: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Dopo:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Anche se non si tratta tecnicamente di una modifica di rilievo, è possibile notare che le differenze nell'output della proprietà Sku.Name degli account di archiviazione restituiti dopo le modifiche apportate a `New/Get/Set-AzStorageAccount` sono le seguenti. Dopo la modifica gli oggetti SkuName di input e di output sono allineati.
  - "StandardLRS" -> "Standard_LRS";
  - "StandardGRS" -> "Standard_GRS";
  - "StandardRAGRS" -> "Standard_RAGRS";
  - "StandardZRS" -> "Standard_ZRS";
  - "PremiumLRS" -> "Premium_LRS";

- Il comportamento predefinito del servizio quando si crea un account di archiviazione senza specificare l'argomento Kind è cambiato.  Nelle versioni precedenti, quando si creava un account di archiviazione senza specificare l'argomento `Kind`, come valore di Kind per l'account di archiviazione si usava `Storage`. Nella nuova versione il valore predefinito di `Kind` è `StorageV2`. Per creare un account di archiviazione V1 in cui Kind è impostato su 'Storage', aggiungere il parametro '-Kind Storage'.

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Esempio: Creare un account di archiviazione (modifica dell'impostazione predefinita di Kind)  

  Prima di:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Dopo:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
