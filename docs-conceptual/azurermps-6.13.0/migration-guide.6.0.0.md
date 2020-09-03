---
title: Modifiche di rilievo in Microsoft Azure PowerShell 6.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 6.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7b14df54d521c12c43663a1a3601e4cb671317b3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241628"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Modifiche di rilievo in Microsoft Azure PowerShell 6.0.0

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell. Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice. Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.

## <a name="table-of-contents"></a>Sommario

- [Modifiche di rilievo di carattere generale](#general-breaking-changes)
  - [Versione minima richiesta di PowerShell innalzata alla 5.0](#minimum-powershell-version-required-bumped-to-50)
  - [Salvataggio automatico del contesto abilitato per impostazione predefinita](#context-autosave-enabled-by-default)
  - [Rimozione dell'alias Tags](#removal-of-tags-alias)
- [Modifiche di rilievo ai cmdlet di AzureRM.Compute](#breaking-changes-to-azurermcompute-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.DataLakeStore](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.Dns](#breaking-changes-to-azurermdns-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.Insights](#breaking-changes-to-azurerminsights-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.KeyVault](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.Network](#breaking-changes-to-azurermnetwork-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.RedisCache](#breaking-changes-to-azurermrediscache-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.Resources](#breaking-changes-to-azurermresources-cmdlets)
- [Modifiche di rilievo ai cmdlet di AzureRM.Storage](#breaking-changes-to-azurermstorage-cmdlets)
- [Moduli rimossi](#removed-modules)
  - [`AzureRM.ServerManagement`](#azurermservermanagement)
  - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Modifiche di rilievo di carattere generale

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Versione minima richiesta di PowerShell innalzata alla 5.0

In precedenza per eseguire qualsiasi cmdlet con Azure PowerShell era necessaria _almeno_ la versione 3.0 di PowerShell. In futuro, questo requisito verrà innalzato alla versione 5.0 di PowerShell. Per informazioni sull'aggiornamento a PowerShell 5.0, vedere [questa tabella](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Salvataggio automatico del contesto abilitato per impostazione predefinita

Per salvataggio automatico del contesto si intende l'archiviazione delle informazioni di accesso di Azure che è possibile usare tra sessioni nuove e diverse di PowerShell. Per altre informazioni sul salvataggio automatico del contesto, vedere [questo documento](/powershell/azure/context-persistence).

In precedenza, il salvataggio automatico del contesto era disabilitato per impostazione predefinita, di conseguenza le informazioni di autenticazione di Azure dell'utente non venivano archiviate tra una sessione e l'altra finché non veniva eseguito il cmdlet `Enable-AzureRmContextAutosave` per attivare la persistenza del contesto. In futuro il salvataggio automatico del contesto verrà abilitato per impostazione predefinita, di conseguenza il contesto degli utenti per i quali _non sono disponibili impostazioni salvate per il salvataggio automatico del contesto_ verrà archiviato al successivo accesso. Gli utenti possono rifiutare esplicitamente questa funzionalità usando il cmdlet `Disable-AzureRmContextAutosave`.

> [!NOTE]
> Questa modifica non riguarderà gli utenti che in precedenza avevano disabilitato il salvataggio automatico del contesto oppure gli utenti con salvataggio automatico del contesto abilitato e contesti esistenti.

### <a name="removal-of-tags-alias"></a>Rimozione dell'alias Tags

L'alias `Tags` per il parametro `Tag` è stato rimosso in numerosi cmdlet. Di seguito è riportato un elenco di moduli (e dei cmdlet corrispondenti) interessati:

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.Compute

**Varie**

- La proprietà del nome dello SKU annidata nei tipi `PSDisk` e `PSSnapshot` è cambiata rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- La proprietà del tipo di account di archiviazione annidata nei tipi `PSVirtualMachine`, `PSVirtualMachineScaleSet` e `PSImage` è cambiata rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**

- I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Add-AzureRmVMDataDisk**

- I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Add-AzureRmVmssDataDisk**

- I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**New-AzureRmAvailabilitySet**
- Il parametro `Managed` è stato rimosso a favore di `Sku`

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**New-AzureRmDiskUpdateConfig**
- I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**New-AzureRmSnapshotConfig**
- I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**New-AzureRmSnapshotUpdateConfig**
- I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Set-AzureRmImageOsDisk**
- I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Set-AzureRmVMAEMExtension**
- Il parametro `DisableWAD` è stato rimosso
    -  Diagnostica di Microsoft Azure è disabilitato per impostazione predefinita

**Set-AzureRmVMDataDisk**
- I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Set-AzureRmVMOSDisk**
- I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Set-AzureRmVmssStorageProfile**
- I valori accettati per il parametro `ManagedDisk` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

**Update-AzureRmVmss**
- I valori accettati per il parametro `ManagedDiskStorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.DataLakeStore

**Export-AzureRmDataLakeStoreItem**
- I parametri `PerFileThreadCount` e `ConcurrentFileCount` sono stati rimossi. In futuro usare il parametro `Concurrency`

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- I parametri `PerFileThreadCount` e `ConcurrentFileCount` sono stati rimossi. In futuro usare il parametro `Concurrency`

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- Il parametro `Clean` è stato rimosso

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.Dns

**New-AzureRmDnsRecordSet**
- Il parametro `Force` è stato rimosso

**Remove-AzureRmDnsRecordSet**
- Il parametro `Force` è stato rimosso

**Remove-AzureRmDnsZone**
- Il parametro `Force` è stato rimosso

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.Insights

**Add-AzureRmAutoscaleSetting**
- Gli alias di parametro `AutoscaleProfiles` e `Notifications` sono stati rimossi

**Add-AzureRmLogProfile**
- Gli alias di parametro `Categories` e `Locations` sono stati rimossi

**Add-AzureRmMetricAlertRule**
- L'alias di parametro `Actions` è stato rimosso

**Add-AzureRmWebtestAlertRule**
- L'alias di parametro `Actions` è stato rimosso

**Get-AzureRmLog**
- Gli alias di parametro `MaxRecords` e `MaxEvents` sono stati rimossi

**Get-AzureRmMetricDefinition**
- L'alias di parametro `MetricNames` è stato rimosso

**New-AzureRmAlertRuleEmail**
- Gli alias di parametro `CustomEmails` e `SendToServiceOwners` sono stati rimossi

**New-AzureRmAlertRuleWebhook**
- L'alias di parametro `Properties` è stato rimosso

**New-AzureRmAutoscaleNotification**
- Gli alias di parametro `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` e `Webhooks` sono stati rimossi

**New-AzureRmAutoscaleProfile**
- Gli alias di parametro `Rules`, `ScheduleDays`, `ScheduleHours` e `ScheduleMinutes` sono stati rimossi

**New-AzureRmAutoscaleWebhook**
- L'alias di parametro `Properties` è stato rimosso

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.KeyVault

**Add-AzureKeyVaultCertificate**
- Il parametro `CertificatePolicy` è diventato obbligatorio.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- Il cmdlet non accetta più parametri singoli che costituiscono il token di accesso, ma sostituisce i parametri di token espliciti, ad esempio `Service` oppure `Permissions`, con un parametro `TemplateUri` generico, che corrisponde a un token di accesso di esempio definito altrove, presumibilmente con i cmdlet PowerShell di Archiviazione o creato manualmente in base alla documentazione di Archiviazione. Il cmdlet mantiene il parametro `ValidityPeriod`.

Per altre informazioni sulla creazione di token di accesso condivisi per Archiviazione di Azure, vedere le pagine della documentazione e in particolare:

- [Creazione di una firma di accesso condiviso del servizio](/rest/api/storageservices/Constructing-a-Service-SAS)
- [Creazione di una firma di accesso condiviso dell'account](/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- Il parametro `IssuerProvider` è diventato obbligatorio.

**Undo-AzureKeyVaultCertificateRemoval**
- L'output di questo cmdlet è cambiato da `CertificateBundle` in `PSKeyVaultCertificate`.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName` è stato rimosso dal set di parametri di `InputObject` e viene invece ottenuto dalla proprietà `ResourceId` del parametro `InputObject`.

**Set-AzureRmKeyVaultAccessPolicy**
- L'autorizzazione `all` è stata rimossa da `PermissionsToKeys`, `PermissionsToSecrets` e `PermissionsToCertificates`.

**Generale**
- La proprietà `ValueFromPipelineByPropertyName` è stata rimossa da tutti i cmdlet in cui era abilitato il piping tramite `InputObject`. I cmdlet interessati sono:
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- I livelli `ConfirmImpact` sono stati rimossi da tutti i cmdlet.  I cmdlet interessati sono:
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Il cmdlet `IKeyVaultDataServiceClient` è stato aggiornato in modo che tutte le operazioni relative ai certificati restituiscano PSTypes invece di tipi SDK. ad esempio:
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.Network


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- Il parametro `ProbeEnabled` è stato rimosso

**Add-AzureRmVirtualNetworkPeering**
- L'alias di parametro `AlloowGatewayTransit` è stato rimosso

**New-AzureRmApplicationGatewayBackendHttpSettings**
- Il parametro `ProbeEnabled` è stato rimosso

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- Il parametro `ProbeEnabled` è stato rimosso

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.RedisCache

**New-AzureRmRedisCache**
- I parametri `Subnet` e `VirtualNetwork` sono stati rimossi a favore di `SubnetId`
- Il parametro `RedisVersion` è stato rimosso
- Il parametro `MaxMemoryPolicy` è stato rimosso a favore di `RedisConfiguration`

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- Il parametro `MaxMemoryPolicy` è stato rimosso a favore di `RedisConfiguration`

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.Resources

**Find-AzureRmResource**
- Questo cmdlet è stato rimosso e la funzionalità è stata spostata in `Get-AzureRmResource`

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Questo cmdlet è stato rimosso e la funzionalità è stata spostata in `Get-AzureRmResourceGroup`

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- Il parametro `AtScopeAndBelow` è stato rimosso.

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Modifiche di rilievo ai cmdlet di AzureRM.Storage

**New-AzureRmStorageAccount**
- Il parametro `EnableEncryptionService` è stato rimosso

**Set-AzureRmStorageAccount**
- I parametri `EnableEncryptionService` e `DisableEncryptionService` sono stati rimossi

## <a name="removed-modules"></a>Moduli rimossi

### `AzureRM.ServerManagement`

Il servizio Strumenti di gestione del server è stato [ritirato lo scorso anno](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), di conseguenza il modulo corrispondente del servizio, `AzureRM.ServerManagement`, è stato rimosso da `AzureRM` e non verrà più distribuito in futuro.

### `AzureRM.SiteRecovery`

Il modulo `AzureRM.SiteRecovery` verrà sostituito da `AzureRM.RecoveryServices.SiteRecovery`, che è un superset funzionale del modulo `AzureRM.SiteRecovery` e include un nuovo set di cmdlet equivalenti. L'elenco completo dei mapping dei vecchi e nuovi cmdlet è disponibile di seguito:

| Cmdlet deprecato                                        | Cmdlet equivalente                                                | Alias                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
