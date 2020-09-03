---
title: Elenco di tutte le modifiche apportate durante la migrazione da AzureRM ad Azure PowerShell Az 1.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche che causano un'interruzione apportate ad Azure PowerShell nel rilascio della versione Az 1.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: ae2539a09b93fb482ed3f8a363c7a0a66e02a412
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239588"
---
# <a name="breaking-changes-for-az-100"></a>Modifiche che causano un'interruzione per Az 1.0.0

Questo documento include informazioni dettagliate sulle modifiche apportate nella migrazione da AzureRM 6.x al nuovo modulo Az 1.x e versioni successive. Il sommario include tutti i passaggi di un percorso di migrazione completo, incluse le modifiche specifiche dei singoli moduli che potrebbero influire sugli script.

Per consigli di carattere generale su come iniziare una migrazione da AzureRM ad Az, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

> [!IMPORTANT]
> Sono state apportate modifiche di rilievo anche tra le versioni 1.0.0 e 2.0.0 di Az. Dopo aver seguito le indicazioni di questa guida per eseguire l'aggiornamento da AzureRM ad Az, vedere l'[elenco delle modifiche di rilievo di Az 2.0.0](migrate-az-2.0.0.md) per sapere se sono necessarie ulteriori modifiche.

## <a name="table-of-contents"></a>Sommario

- [Modifiche di rilievo di carattere generale](#general-breaking-changes)
  - [Modifiche apportate al prefisso dei nomi dei cmdlet](#cmdlet-noun-prefix-changes)
  - [Modifiche ai nomi dei moduli](#module-name-changes)
  - [Moduli rimossi](#removed-modules)
  - [Windows PowerShell 5.1 e .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Rimozione temporanea dell'accesso utente con PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Accesso predefinito del codice dispositivo anziché del prompt del Web browser](#default-device-code-login-instead-of-web-browser-prompt)
- [Modifiche che causano un'interruzione dei moduli](#module-breaking-changes)
  - [Az.ApiManagement (in precedenza AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (in precedenza AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (in precedenza AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (in precedenza AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (in precedenza AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (in precedenza AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (in precedenza AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (in precedenza AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (in precedenza AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Modifiche di rilievo di carattere generale

Questa sezione illustra in dettaglio le modifiche di rilievo di carattere generale incluse nella riprogettazione del modulo Az.

### <a name="cmdlet-noun-prefix-changes"></a>Modifiche al prefisso dei nomi dei cmdlet

Nel modulo AzureRM come prefisso dei nomi dei cmdlet si usava `AzureRM` o `Azure`.  Az semplifica e normalizza i nomi dei cmdlet, in modo che tutti i cmdlet usino 'Az' come prefisso dei nomi dei cmdlet. Ad esempio:

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

È stato modificato in:

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

Per semplificare la transizione a questi nuovi nomi dei cmdlet, Az introduce due nuovi cmdlet, ovvero [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) e [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).  `Enable-AzureRmAlias` crea gli alias per i nomi dei cmdlet precedenti in AzureRM per i quali viene eseguito il mapping ai nuovi nomi dei cmdlet Az. Se si usa l'argomento `-Scope` con `Enable-AzureRmAlias`, è possibile scegliere dove abilitare gli alias.

Ad esempio, lo script seguente in AzureRM:

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Può essere eseguito con modifiche minime usando `Enable-AzureRmAlias`:

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

L'esecuzione di `Enable-AzureRmAlias -Scope CurrentUser` abilita gli alias per tutte le sessioni di PowerShell che vengono aperte, in modo che dopo l'esecuzione di questo cmdlet non sarà necessario modificare uno script simile al seguente:

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Per informazioni dettagliate sull'utilizzo dei cmdlet alias, vedere la [guida di riferimento per Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

Quando si è pronti per disabilitare gli alias, usare `Disable-AzureRmAlias` per rimuovere gli alias creati. Per informazioni dettagliate, vedere la [guida di riferimento per Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Quando si disabilitano gli alias, assicurarsi che vengano disabilitati per _tutti_ gli ambiti in cui erano abilitati.

### <a name="module-name-changes"></a>Modifiche ai nomi dei moduli

I nomi dei moduli sono stati modificati da `AzureRM.*` a `Az.*`, fatta eccezione per i moduli seguenti:

| Modulo AzureRM | Modulo Az |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

Le modifiche nei nomi dei moduli significano che tutti gli script che usano `#Requires` o `Import-Module` per caricare moduli specifici dovranno essere modificati per usare il nuovo modulo. Per i moduli in cui il suffisso del cmdlet non è cambiato, anche se il nome del modulo è cambiato il suffisso che indica lo spazio dell'operazione _non_ ha subito variazioni.

#### <a name="migrating-requires-and-import-module-statements"></a>Migrazione delle istruzioni #Requires e Import-Module

Gli script che usano `#Requires` o `Import-Module` per dichiarare una dipendenza dai moduli AzureRM devono essere aggiornati in modo che usino i nuovi nomi dei moduli. Ad esempio:

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

Devono essere modificati in:

```azurepowershell-interactive
#Requires -Module Az.Compute
```

Per `Import-Module`:

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

Devono essere modificati in:

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migrazione delle chiamate dei cmdlet complete

Gli script che usano le chiamate dei cmdlet qualificate di modulo, come:

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

Devono essere modificati in modo che usino i nuovi nomi dei moduli e dei cmdlet:

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migrazione delle dipendenze del manifesto del modulo

I moduli che esprimono le dipendenze dai moduli AzureRM tramite un file del manifesto del modulo (con estensione psd1) dovranno aggiornare i nomi dei moduli nella sezione `RequiredModules`:

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Devono essere modificati in:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Moduli rimossi

I moduli seguenti sono stati rimossi:

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Gli strumenti per questi servizi non sono più supportati attivamente.  I clienti sono invitati a passare a servizi alternativi non appena possibile.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 e .NET 4.7.2

Per usare Az con PowerShell 5.1 per Windows è richiesta l'installazione di .NET Framework 4.7.2. Se invece si usa PowerShell Core 6.x o versioni successive, .NET Framework non è richiesto.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Rimozione temporanea dell'accesso utente con PSCredential

A causa delle modifiche nel flusso di autenticazione per .NET Standard verrà temporaneamente rimosso l'accesso utente tramite PSCredential. Questa funzionalità sarà reintrodotta nella versione del 15/01/2019 per PowerShell 5.1 per Windows. Questa modifica è descritta in dettaglio in [questo problema di GitHub](https://github.com/Azure/azure-powershell/issues/7430).

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Accesso predefinito del codice dispositivo anziché del prompt del Web browser

A causa delle modifiche nel flusso di autenticazione per .NET Standard, viene usato l'accesso del dispositivo come flusso di accesso predefinito durante l'accesso interattivo. L'accesso basato su Web browser verrà reintrodotto per PowerShell 5.1 per Windows come impostazione predefinita nella versione del 15/01/2019. A quel punto, gli utenti potranno scegliere l'accesso del dispositivo usando un parametro Switch.

## <a name="module-breaking-changes"></a>Modifiche che causano un'interruzione dei moduli

Questa sezione illustra in dettaglio le modifiche di rilievo per singoli cmdlet e moduli.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (in precedenza AzureRM.ApiManagement)

- Sono stati rimossi i cmdlet seguenti:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Usare il cmdlet **Set-AzApiManagement** per impostare queste proprietà
- Sono state rimosse le proprietà seguenti:
  - Sono state rimosse le proprietà `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` di tipo `PsApiManagementHostnameConfiguration` da `PsApiManagementContext`. Usare `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` di tipo `PsApiManagementCustomHostNameConfiguration`.
  - È stata rimossa la proprietà `StaticIPs` da PsApiManagementContext. La proprietà è stata suddivisa in `PublicIPAddresses` e `PrivateIPAddresses`.
  - È stata rimossa la proprietà obbligatoria `Location` dal cmdlet New-AzureApiManagementVirtualNetwork.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)

- Il parametro `InvoiceName` è stato rimosso dal cmdlet `Get-AzConsumptionUsageDetail`.  Gli script dovranno usare altri parametri di identità per la fatturazione.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)

- È stato rimosso il set di parametri `GetSkusWithAccountParamSetName` dal cmdlet `Get-AzCognitiveServicesAccountSkus`.  È necessario ottenere gli SKU per tipo di account e posizione, anziché usare ResourceGroupName e nome account.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (in precedenza AzureRM.Compute)

- `IdentityIds` è stato rimosso dalla proprietà `Identity` negli oggetti `PSVirtualMachine` e `PSVirtualMachineScaleSet`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.
- Il tipo della proprietà `InstanceView` dell'oggetto `PSVirtualMachineScaleSetVM` è stato modificato da `VirtualMachineInstanceView` a `VirtualMachineScaleSetVMInstanceView`
- Le proprietà `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` sono state rimosse dalla proprietà `UpgradePolicy`
- Il tipo della proprietà `Sku` nell'oggetto `PSSnapshotUpdate` è stato modificato da `DiskSku` a `SnapshotSku`
- `VmScaleSetVMParameterSet` è stato rimosso dal cmdlet `Add-AzVMDataDisk`. Non è più possibile aggiungere singolarmente un disco dati a una macchina virtuale del set di scalabilità.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)

- Il parametro `GatewayName` è diventato obbligatorio nel cmdlet `New-AzDataFactoryEncryptValue`
- È stato rimosso il cmdlet `New-AzDataFactoryGatewayKey`
- È stato rimosso il parametro `LinkedServiceName` dal cmdlet `Get-AzDataFactoryV2ActivityRun`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)

- Sono stati rimossi i cmdlet deprecati: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` e `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)

- Il tipo del parametro `Encoding` dei cmdlet seguenti è stato modificato da `FileSystemCmdletProviderEncoding` a `System.Text.Encoding`. Questa modifica rimuove i valori di codifica `String` e `Oem`. Tutti gli altri valori di codifica precedenti rimangono.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- È stato rimosso l'alias della proprietà `Tags` deprecata dai cmdlet `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`

  Lo script che usa
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Deve essere modificato in
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Sono state rimosse le proprietà deprecate `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` dall'oggetto `PSDataLakeStoreAccountBasic`.  Tutti gli script che usano `PSDatalakeStoreAccount` restituito da `Get-AzDataLakeStoreAccount` non devono fare riferimento a queste proprietà.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (in precedenza AzureRM.KeyVault)

- La proprietà `PurgeDisabled` è stata rimossa dagli oggetti `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes`. Gli script non devono più fare riferimento alla proprietà ```PurgeDisabled``` per le decisioni di elaborazione.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (in precedenza AzureRM.Media)

- È stato rimosso l'alias della proprietà `Tags` deprecata dal cmdlet `New-AzMediaService`. Lo script che usa
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Deve essere modificato in
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (in precedenza AzureRM.Insights)

- Sono stati rimossi i nomi plurali del parametro `Categories` e `Timegrains` sostituendoli con nomi di parametro singolari dal cmdlet `Set-AzDiagnosticSetting`. Lo script che usa
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Deve essere modificato in
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (in precedenza AzureRM.Network)

- È stato rimosso il parametro `ResourceId` deprecato dal cmdlet `Get-AzServiceEndpointPolicyDefinition`
- È stata rimossa la proprietà `EnableVmProtection` deprecata dall'oggetto `PSVirtualNetwork`
- È stato rimosso il cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig` deprecato

Gli script non devono più prendere decisioni di elaborazione in base ai valori di questi campi.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)

- Il set di parametri predefinito per `Get-AzOperationalInsightsDataSource` è stato rimosso e `ByWorkspaceNameByKind` è diventato il set di parametri predefinito

  Gli script che elencano le origini dati usando
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  Devono essere modificati per specificare un tipo
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)

- È stato rimosso il parametro `Encryption` dal cmdlet `New/Set-AzRecoveryServicesAsrPolicy`
- Il parametro `TargetStorageAccountName` è ora obbligatorio per il ripristino dei dischi gestiti nel cmdlet `Restore-AzRecoveryServicesBackupItem`
- Sono stati rimossi i parametri `StorageAccountName` e `StorageAccountResourceGroupName` nel cmdlet `Restore-AzRecoveryServicesBackupItem`
- È stato rimosso il parametro `Name` nel cmdlet `Get-AzRecoveryServicesBackupContainer`

### <a name="azresources-previously-azurermresources"></a>Az.Resources (in precedenza AzureRM.Resources)

- È stato rimosso il parametro `Sku` dal cmdlet `New/Set-AzPolicyAssignment`
- È stato rimosso il parametro `Password` dal cmdlet `New-AzADServicePrincipal` e `New-AzADSpCredential`. Le password vengono generate automaticamente e gli script che fornivano la password:

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Devono essere modificati per recuperare la password dall'output:

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)

- Sono stati modificati i tipi restituiti di cmdlet seguenti:
  - La proprietà `ServiceTypeHealthPolicies` di tipo `ApplicationHealthPolicy` è stata rimossa.
  - La proprietà `ApplicationHealthPolicies` di tipo `ClusterUpgradeDeltaHealthPolicy` è stata rimossa.
  - La proprietà `OverrideUserUpgradePolicy` di tipo `ClusterUpgradePolicy` è stata rimossa.
  - Queste modifiche interessano i cmdlet seguenti:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (in precedenza AzureRM.Sql)

- Sono stati rimossi i parametri `State` e `ResourceId` dal cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Sono stati rimossi i cmdlet deprecati: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`
- È stato rimosso il parametro `Current` deprecato dal cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`
- È stato rimosso il parametro `DatabaseName` deprecato dal cmdlet `Get-AzSqlServerServiceObjective`
- È stato rimosso il parametro `PrivilegedLogin` deprecato dal cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)

- Per supportare la creazione di un contesto di archiviazione Oauth con solo il nome dell'account di archiviazione, il set di parametri predefinito è stato modificato in `OAuthParameterSet`
  - Esempio: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- Il parametro `Location` è diventato obbligatorio nel cmdlet `Get-AzStorageUsage`
- I metodi dell'API di archiviazione usano ora il Modello asincrono basato su attività (TAP), invece delle chiamate API sincrone. Gli esempi seguenti illustrano i nuovi comandi asincroni:

#### <a name="blob-snapshot"></a>Snapshot del BLOB

Modulo AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Modulo Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Snapshot di condivisione

Modulo AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Modulo Az:

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Annullare l'eliminazione del BLOB eliminato temporaneamente

Modulo AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Modulo Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Impostare il livello di BLOB

Modulo AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Modulo Az:

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (in precedenza AzureRM.Websites)

- Sono state rimosse le proprietà deprecate dagli oggetti `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite`
