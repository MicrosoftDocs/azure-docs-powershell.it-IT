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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853458"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

---
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