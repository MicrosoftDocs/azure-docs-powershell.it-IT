---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368178"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

---
## <a name="660---july-2018"></a>6.6.0 - Luglio 2018
#### <a name="general"></a>Generale
* Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione. L'impostazione predefinita è sempre true, risorse individuali e override del valore predefinito.
* Aggiunta dei tipi ps1xml a Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Supporto del recupero del contesto di archiviazione da DefaulfProfile
* Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370
    - Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract
* Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515
    - Correzione del bug in File.Save per evitare l'overload con il tipo di codifica
* Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560
    - Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId

#### <a name="azurermcompute"></a>AzureRM.Compute
* Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.
* Correzione del cmdlet Invoke-AzureRmVMRunCommand
* Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.  Il parametro ResouceGroupName è ora facoltativo.
* Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.
* Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.
* Aggiornamento dell'esempio per New-AzureRmDisk
* Aggiunta dell'esempio per 'New-AzureRmVM'
* Aggiornamento della descrizione per Set-AzureRmVMOSDisk
* Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Aggiornamento della versione di ADF .Net SDK a 1.1.0.
* Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.
     - Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione

#### <a name="azurerminsights"></a>AzureRM.Insights
* Correzione della formattazione di OutputType nei file della Guida
* Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'
    - https://github.com/Azure/azure-powershell/issues/6765
* Correzione dello scenario di piping con 'Set-AzureRmResource'

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione
* Correzione di alcuni problemi
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule
* Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog

#### <a name="azurermstorage"></a>AzureRM.Storage
* Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet
* Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - Luglio 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'

#### <a name="azurestorage"></a>Azure.Storage
* Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'

#### <a name="azurermcompute"></a>AzureRM.Compute
* Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet
* Aggiunta di un esempio per 'Add-AzureRmVmssExtension'
* Aggiunta di esempi per 'Remove-AzureRmVmssExtension'
* Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'
* Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering
* Aggiornamento dei cmdlet seguenti per il gateway applicazione
    - New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone
    - New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2
    - Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2
* Rigenerazione del cmdlet RouteTable con la versione più recente del generatore

#### <a name="azurermrelay"></a>AzureRM.Relay
* Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio

#### <a name="azurermresources"></a>AzureRM.Resources
* Aggiornamento dei cmdlet roleassignment e roledefinition:
    - Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.
* Correzione del cmdlet Get-AzureRmRoleAssignment
    - Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups
* Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Aggiunta del parametro top e skip ai cmdlet list
* Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'

#### <a name="azurermsql"></a>AzureRM.Sql
* Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.
* Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`
* `Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida

## <a name="640---july-2018"></a>6.4.0 - Luglio 2018
#### <a name="general"></a>Generale
* Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli

#### <a name="azurermprofile"></a>AzureRM.Profile
* Aggiunta dell'attributo Ps1Xml ai tipi di output di base

#### <a name="azurermcompute"></a>AzureRM.Compute
* Funzionalità tag IP per VMSS
    - Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'
    - Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig
* Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS
    - Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss
* Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss
    - Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties
* Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive
* Correzione della posizione del test dei cmdlet di DataLake

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup
* Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi. Aggiunta di un set di parametri predefinito.
* Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag

#### <a name="azurermnetwork"></a>AzureRM.Network
* Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona
* Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM
    - Aggiunta di Get-AzureRmExpressRouteCrossConnection
    - Aggiunta di Set-AzureRmExpressRouteCrossConnection
    - Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering
    - Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering
    - Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering
    - Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable
    - Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus. Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione. Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.

#### <a name="azurermresources"></a>AzureRM.Resources
* Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:
    - Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione
    - Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione
    - Aggiunta delle opzioni -Effective e -All al parametro di controllo
* Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition
    - Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico
    - Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica
* Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition
    - Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico
    - Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica
* Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'
* Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'
    - https://github.com/Azure/azure-powershell/issues/6505
* Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.

#### <a name="azurermsql"></a>AzureRM.Sql
* Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint
* Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet

## <a name="630---june-2018"></a>6.3.0 - Giugno 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave
* Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente

#### <a name="azurestorage"></a>Azure.Storage
* Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati 
* Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Versione pubblica dei cmdlet di Policy Insights
    - Uso della versione API 2018-04-04
    - Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup. Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity
* 'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo

## <a name="621---june-2018"></a>6.2.1 - Giugno 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro

## <a name="620---june-2018"></a>6.2.0 - Giugno 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo

#### <a name="azurermcompute"></a>AzureRM.Compute
* Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali
    - Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"
    - Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:
    - Aggiunta dell'operazione di configurazione del repository della factory
    - Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret
    - Aggiornamento di diversi tipi di modello da SecretBase a Object
    - Aggiunta del trigger di eventi BLOB

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Aggiornamento della documentazione con output di esempio

### <a name="azurermnetwork"></a>AzureRM.Network
* Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher

#### <a name="azurermresources"></a>AzureRM.Resources
* Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob

### <a name="azurermsql"></a>AzureRM.Sql
* Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy

## <a name="610---may-2018"></a>6.1.0 - Maggio 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions
* Aggiunta di supporto per il back-end di Service Fabric
* Aggiunta di supporto per il logger di Application Insights
* Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API
* Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA
* Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy
* Aggiunta di supporto per identità di MSI
* Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts
* Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties
* Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry 
* Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview
* Aggiunta di un cmdlet per la creazione della configurazione del protocollo
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Aggiunta di un cmdlet per il recupero di una connessione a circuito
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups
* Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata. Inviare la richiesta con i nuovi criteri di conservazione flessibili'.
* Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.
* I cmdlet aggiornati includono: 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.