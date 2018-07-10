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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406484"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

---
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