---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 34b21292ccc47bb53b6609cd637ef18338a45cd3
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121466"
---
# <a name="azure-powershell-release-notes"></a>Note sulla versione di Azure PowerShell
## <a name="180---april-2019"></a>1.8.0 - Aprile 2019
### <a name="highlights-since-the-last-major-release"></a>Novità rispetto all'ultima versione principale
* Disponibilità generale del modulo `Az`
* Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce
* Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network
* Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1
* Aggiunta del supporto per i runbook Python 2 in Az.Automation
* Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch

#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac

#### <a name="azbatch"></a>Az.Batch
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azcdn"></a>Az.Cdn
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azcompute"></a>Az.Compute
* Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.
* Correzione della documentazione per i caratteri jolly

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azeventgrid"></a>Az.EventGrid
* Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.

#### <a name="azeventhub"></a>Az.EventHub
* Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi

#### <a name="azhdinsight"></a>Az.HDInsight
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="aziothub"></a>Az.IotHub
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azkeyvault"></a>Az.KeyVault
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.
* Correzione della documentazione per i caratteri jolly

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azmedia"></a>Az.Media
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azmonitor"></a>Az.Monitor
  * Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Aggiornamento di Monitor SDK alla versione 0.22.0-preview

#### <a name="aznetwork"></a>Az.Network
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.
* Correzione della documentazione per i caratteri jolly

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.
* Aggiornamento del formato tabella per SQL in VM Azure
* Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare
* Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario

#### <a name="azrediscache"></a>Az.RedisCache
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.

#### <a name="azresources"></a>Az.Resources
* Correzione della documentazione per i caratteri jolly

#### <a name="azsql"></a>Az.Sql
* Sostituzione della dipendenza da Monitor SDK con codice comune
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.
* Elaborazione avanzata della classificazione di più colonne.
* Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.
* Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.
* Supporto per il parametro del fuso orario nella creazione di istanze gestite.
* Correzione della documentazione per i caratteri jolly

#### <a name="azwebsites"></a>Az.Websites
* Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione
* Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.
* Aggiornamento di WebSites SDK.
* Rimozione della proprietà AdminSiteName da PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 - Aprile 2019
### <a name="highlights-since-the-last-major-release"></a>Novità rispetto all'ultima versione principale
* Disponibilità generale del modulo `Az`
* Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce
* Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network
* Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1
* Aggiunta del supporto per i runbook Python 2 in Az.Automation
* Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch

#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale
* Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione

#### <a name="azautomation"></a>Az.Automation
* Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni. Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.
* Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure

#### <a name="azcompute"></a>Az.Compute
* Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig
* Creazione di VM consentita con l'immagine della raccolta di altri tenant.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .Net SDK alla versione 3.0.2
* Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'
* Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'
    - Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856
* Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Supporto della classificazione di dati del database.

#### <a name="azstorage"></a>Az.Storage
* Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso
    - New-AzStorageContext
* Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 - Marzo 2019
### <a name="highlights-since-the-last-major-release"></a>Novità rispetto all'ultima versione principale
* Disponibilità generale del modulo `Az`
* Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce
* Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network
* Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1
* Aggiunta del supporto per i runbook Python 2 in Az.Automation
* Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch

#### <a name="azautomation"></a>Az.Automation
* Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:
    * Raggruppamento dinamico
    * Script pre-post
    * Impostazione di riavvio

#### <a name="azcompute"></a>Az.Compute
* Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData
* Aggiornamento della libreria client di Calcolo a 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure
* Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP
* Aggiunta del supporto di pipe per annullare la registrazione di contenitori

#### <a name="azresources"></a>Az.Resources
* Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup
* Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM

#### <a name="azsql"></a>Az.Sql
* Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.

#### <a name="azstorage"></a>Az.Storage
* Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"

## <a name="150---march-2019"></a>1.5.0 - Marzo 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest
* Aggiornamento degli esempi per Connect-AzAccount

#### <a name="azautomation"></a>Az.Automation
* Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure
* Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi. Ora restituisce tutti i nodi.

#### <a name="azcdn"></a>Az.Cdn
* Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati

#### <a name="azcompute"></a>Az.Compute
* Aggiunta del supporto dei caratteri jolly ai cmdlet Get

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .Net SDK alla versione 3.0.1

#### <a name="azlogicapp"></a>Az.LogicApp
* Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del supporto dei caratteri jolly ai cmdlet Network

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure
* Aggiornamento di SDK
* Rimozione del controllo VMappContainer in Get-ProtectableItem
* Aggiunta di Name e ServerName come parametri per Get-ProtectableItem

#### <a name="azresources"></a>Az.Resources
* Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933
* Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240
* Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* Aggiornamento di AuditingEndpointsCommunicator.
    - Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.

#### <a name="azstorage"></a>Az.Storage
* Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 - Febbraio 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Cmdlet AddAzureASAccount deprecato

#### <a name="azautomation"></a>Az.Automation
* Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration
* Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration
* Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.

#### <a name="azcompute"></a>Az.Compute
* Correzione del problema dei set di parametri ID
* Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name
* Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage
* Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati

#### <a name="azeventhub"></a>Az.EventHub
* Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub

#### <a name="azkeyvault"></a>Az.KeyVault
* Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret

#### <a name="azlogicapp"></a>Az.LogicApp
* Aggiunta dello SKU Basic per gli account di integrazione
* Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid
* Nuovi cmdlet per gli assembly di account di integrazione
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Nuovi cmdlet per la configurazione batch degli account di integrazione
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0

#### <a name="azmonitor"></a>Az.Monitor
* Aggiornamento della Guida per Get-AzMetric

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.
    - Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.
    - Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.

#### <a name="azresources"></a>Az.Resources
* correzione del problema https://github.com/Azure/azure-powershell/issues/8166
* correzione del problema https://github.com/Azure/azure-powershell/issues/8235
* correzione del problema https://github.com/Azure/azure-powershell/issues/6219
* Correzione del bug che impedisce di ripetere la creazione di KeyCredentials

#### <a name="azsql"></a>Az.Sql
* Aggiunta del supporto per il livello Hyperscale del database SQL
* Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta

#### <a name="azwebsites"></a>Az.Websites
* Correzione dell'esempio in Get-AzWebAppSlotMetrics

## <a name="130---february-2019"></a>1.3.0 - Febbraio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento alla versione più recente di ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Disponibilità generale del modulo Az.AnalysisServices.

#### <a name="azcompute"></a>Az.Compute
* Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80
* Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics
* Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Disponibilità generale del modulo Az.RecoveryServices.

#### <a name="azresources"></a>Az.Resources
* Correzione dei contrassegni per i gruppi di risorse
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166
* Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL
* Correzione dell'eccezione nullref in Get-AzSqlCapability

## <a name="121---january-2019"></a>1.2.1 - Gennaio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Rilascio con la versione corretta dell'autenticazione

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Rilascio con la dipendenza aggiornata dell'autenticazione

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Rilascio con la dipendenza aggiornata dell'autenticazione

## <a name="120---january-2019"></a>1.2.0 - Gennaio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1
* Aggiornamento degli URL errati della Guida in linea
* Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm

#### <a name="azaks"></a>Az.Aks
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azautomation"></a>Az.Automation
* Aggiunta del supporto dei runbook Python 2
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azcdn"></a>Az.Cdn
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azcompute"></a>Az.Compute
* Aggiunta del cmdlet Invoke-AzVMReimage
* Aggiunta del parametro TempDisk a Set-AzVmss
* Correzione del messaggio di avviso di New-AzVM

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .Net SDK alla versione 3.0.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462
* Aggiornamento degli URL errati della Guida in linea

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Aggiornamento degli URL errati della Guida in linea

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azresources"></a>Az.Resources
* Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"
* Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse
* Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode
* Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747
* Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932
* Correzione di alcuni messaggi di errore.
* Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.
* Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.

#### <a name="azsignalr"></a>Az.SignalR
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azsql"></a>Az.Sql
* Aggiornamento degli URL errati della Guida in linea
* Aggiornamento della descrizione del parametro LicenseType con i valori possibili
* Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata
* Supporto delle regole di confronto personalizzate nell'istanza gestita

#### <a name="azstorage"></a>Az.Storage
* Aggiornamento degli URL errati della Guida in linea
* Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Aggiornamento degli URL errati della Guida in linea

#### <a name="azwebsites"></a>Az.Websites
* Aggiornamento degli URL errati della Guida in linea
* Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.
* Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app

## <a name="110---january-2019"></a>1.1.0 - Gennaio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias

#### <a name="azcompute"></a>Az.Compute
* Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage
* Aggiornamento della descrizione dell'ID nei file della Guida
* Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.
    - Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono

#### <a name="azeventgrid"></a>Az.EventGrid
* Aggiornamento per l'uso della versione API 2019-01-01.
* Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01
    - New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:
        - Durata (TTL) dell'evento
        - Numero massimo di tentativi di recapito per gli eventi
        - Endpoint di messaggi non recapitabili
    - Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:
        - Durata (TTL) dell'evento
        - Numero massimo di tentativi di recapito per gli eventi
        - Endpoint di messaggi non recapitabili
* Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.
* Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.

#### <a name="aziothub"></a>Az.IotHub
* Aggiornamento alla versione più recente dell'SDK IotHub

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp elenca tutto senza nome specificato

#### <a name="azresources"></a>Az.Resources
* Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875
* Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition
* Correzione di un errore di battitura nella documentazione di New-AzDeployment
* Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts

#### <a name="azsql"></a>Az.Sql
* Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.

#### <a name="azstorage"></a>Az.Storage
* Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous
    - New-AzStorageContext
* Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'
* Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts

## <a name="100---december-2018"></a>1.0.0 - Dicembre 2018
### <a name="general"></a>Generale

- Disponibilità generale del modulo Az
- Guida per ogni modulo
- Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)
- Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM

### <a name="azaccounts"></a>Az.Accounts
- Modificato da Az.Profile
- Correzione dei formati di tabella per i tipi di profilo e di contesto

### <a name="azapimanagement"></a>Az.ApiManagement
- Correzioni per #7002
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azbatch"></a>Az.Batch
- Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.
- Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azbilling"></a>Az.Billing
- Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azcognitivservices"></a>Az.CognitivServices
- Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount
- Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Aggiunta del supporto di ManagedIdentity

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azmonitor"></a>Az.Monitor
- Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azkeyvault"></a>Az.KeyVault
- Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output

### <a name="azmachinelearning"></a>Az.MachineLearning
- Inclusione dei cmdlet del modulo Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Rimozione dell'alias -Tags deprecato dai New-AzMediaService

### <a name="aznetwork"></a>Az.Network
Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione
    - Nuovi cmdlet aggiunti:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.
    - Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azprofile"></a>Az.Profile
- Modifica del nome del modulo in Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azresources"></a>Az.Resources
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azservicefabric"></a>Az.ServiceFabric
- Supporto della specifica del certificato per nome comune e identificazione personale
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azsignalr"></a>Az.SIgnalR
- Disponibilità generale per i cmdlet di PowerShell per SIgnalR

### <a name="azsql"></a>Az.Sql
- Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce
- Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azstorage"></a>Az.Storage
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

### <a name="azwebsites"></a>Az.Websites
- Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)

## <a name="070---december-2018"></a>0.7.0 - Dicembre 2018

### <a name="general"></a>Generale

* Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az

### <a name="azcompute"></a>Az.Compute

* Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Correzione della barra finale del dominio dell'account adls

### <a name="azfrontdoor"></a>Az.FrontDoor

* Correzione di alcuni collegamenti interrotti
    - Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.
    - Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.
* storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.

### <a name="azresources"></a>Az.Resources

* Correzione per https://github.com/Azure/azure-powershell/issues/7679
    - Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.

### <a name="azsql"></a>Az.Sql

* Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az
* Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core
* Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.

### <a name="azstorage"></a>Az.Storage

* Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount
* Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext
    - Start-AzureStorageFileCopy
* Supporto della configurazione del sito Web statico
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp e Set-AzureRmWebAppSlot
    - È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux. Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.

## <a name="061---november-2018"></a>0.6.1 - Novembre 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Aggiornamento delle dipendenze per problemi di mapping dei tipi

### <a name="azautomation"></a>Az.Automation
* Cmdlet di Automazione di Azure basati su Swagger
* Aggiunta di cmdlet di Gestione aggiornamenti
* Aggiunta di cmdlet di controllo del codice sorgente
* Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup
* Risoluzione dei problemi del comando Node per il registro DSC

### <a name="azcompute"></a>Az.Compute
* Risoluzione del problema relativo all'identità per l'identità SystemAssigned
* Aggiornamento delle dipendenze per problemi di mapping dei tipi

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Aggiornamento delle dipendenze per problemi di mapping dei tipi

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace

### <a name="aznetwork"></a>Az.Network
* Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError
* Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati
* Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.
* Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.
* Conversione del fuso orario dei criteri in caratteri maiuscoli.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem
* Aggiornamento delle dipendenze per problemi di mapping dei tipi

### <a name="azrelay"></a>Az.Relay
* Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.

### <a name="azresources"></a>Az.Resources
* Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`
* Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata
* Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione

### <a name="azsql"></a>Az.Sql
* Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Abilitazione della gestione dei criteri di controllo estesi in un server o un database.
    - Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.
    - Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione

## <a name="050---november-2018"></a>0.5.0 - Novembre 2018
#### <a name="general"></a>Generale
* Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo

#### <a name="azprofile"></a>Az.Profile
* Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime
* Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId
* Aggiornamento della descrizione di TenantId per Connect-AzAccount
* Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant
    - https://github.com/Azure/azure-powershell/issues/6936
* Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant
    - https://github.com/Azure/azure-powershell/issues/7453
* Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita
    - https://github.com/Azure/azure-powershell/issues/7462
* Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk
* Get-AzVMImage mostra AutomaticOSUpgradeProperties
* Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiornamento del pacchetto DataLake alla versione 1.1.10.
* Aggiunta della concorrenza predefinita alle operazioni multithreading.

#### <a name="azinsights"></a>Az.Insights
* Correzione del problema numero 7267 (area Ridimensionamento automatico)
    - Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).
* Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione
    - Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato

#### <a name="aznetwork"></a>Az.Network
* Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Aggiunta di cmdlet di correzione dei criteri

#### <a name="azresources"></a>Az.Resources
* Correzione per https://github.com/Azure/azure-powershell/issues/7402
    - È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'

#### <a name="azservicebus"></a>Az.ServiceBus
* Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.
* Correzione di 'Add-AzServiceFabricClusterCertificate'
    - Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).
    - Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).
* Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.

## <a name="040---october-2018"></a>0.4.0 - Ottobre 2018
#### <a name="azprofile"></a>Az.Profile
* Risoluzione del problema con Get-AzSubscription in CloudShell
* Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime

#### <a name="azcompute"></a>Az.Compute
* Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'
* Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiunta del supporto per le regole di rete virtuale
    - Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.
    - Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.
* Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.

#### <a name="azresources"></a>Az.Resources
* Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito. Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.

## <a name="030---october-2018"></a>0.3.0 - Ottobre 2018
#### <a name="azurestorage"></a>Azure.Storage
* Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto
    - Get-AzStorageUsage

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.

#### <a name="azcompute"></a>Az.Compute
* Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati
* Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.
* Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Aggiornamento di ADF .Net SDK alla versione 2.3.0

#### <a name="aznetwork"></a>Az.Network
* Aggiunta della funzionalità NetworkProfile e di nuovi cmdlet
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Aggiunta del collegamento di associazione di servizio nel modello di subnet
* Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap
* Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig

#### <a name="azrediscache"></a>Az.RedisCache
* Possibilità di usare in futuro qualsiasi stringa come parametro Size. Aggiunta di P5 nel popup PSArgumentCompleter

#### <a name="azresources"></a>Az.Resources
* Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition
* Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User

#### <a name="azsql"></a>Az.Sql
* Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente

#### <a name="azwebsites"></a>Az.Websites
* Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori
* Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows

## <a name="020---september-2018"></a>0.2.0 - Settembre 2018
 Versione iniziale
