---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: c02cfaa7f7f39393f21cec31c5115f009381b19c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "81446054"
---
# <a name="azure-powershell-release-notes"></a>Note sulla versione di Azure PowerShell
## <a name="0100-preview---april-2020"></a>0.10.0-preview - Aprile 2020
### <a name="general"></a>Generale
* Disponibilità di moduli Az in anteprima nell'hub di Azure Stack. Consentono la compatibilità multipiattaforma con Linux e macOS. L'hub di Azure Stack ora supporta PowerShell core con i moduli Az. Per altre informazioni, vedere [qui](https://aka.ms/az4AzureStack)
* I moduli Az supportano il profilo 2019-03-01-ibrido:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* Sono stati introdotti tre nuovi moduli di PowerShell per az compatibili con l'hub di Azure Stack, ovvero Az.Databox, Az.IotHub e Az.EventHub
* I comandi rimangono relativamente invariati, con modifiche minime come la sostituzione di AzureRM con Az
* Il collegamento aggiornato alla documentazione di PowerShell per l'hub di Azure Stack è reperibile [qui](aka.ms/InstallASHPowerShell)

#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento da ADAL a MSAL


## <a name="370---march-2020"></a>3.7.0 - Marzo 2020
#### <a name="azaccounts"></a>Az.Accounts
* Correzione dell'eccezione NullReferenceException generata da 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' in caso di mancato accesso [#10292]

#### <a name="azcompute"></a>Az.Compute
* Aggiunta dei parametri seguenti al cmdlet 'New-AzDiskConfig': 
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Proprietà Encryption consentita per il parametro Target del cmdlet 'New-AzGalleryImageVersion'.
* Correzione del problema tempDisk per i cmdlet 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'. [#11354]
* Aggiunta del supporto dei cmdlet seguenti per la nuova estensione SAP
    - 'Set-AzVMAEMExtension'
    - 'Get-AzVMAEMExtension'
    - 'Remove-AzVMAEMExtension'
    - 'Update-AzVMAEMExtension'
* Correzione di errori negli esempi del documento della Guida
* Visualizzazione del valore stringa esatto per PowerState VM nel formato tabella.
* 'New-AzVmssConfig': correzione della serializzazione della proprietà AutomaticRepairs quando SinglePlacementGroup è disabilitato. [#11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .NET SDK alla versione 4.8.0
* Aggiunta di parametri facoltativi al comando 'Invoke-AzDataFactoryV2Pipeline' per supportare la riesecuzione

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiunta della descrizione della modifica di rilievo per 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'
* Aggiunta dell'opzione di codifica Byte per 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'

#### <a name="azhdinsight"></a>Az.HDInsight
* Supporto della versione minima supportata di TLS durante la creazione del cluster.

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta del supporto per gestire le impostazioni distribuite per singolo dispositivo. I nuovi cmdlet sono:
    - 'Get-AzIotHubDistributedTracing'
    - 'Set-AzIotHubDistributedTracing'

#### <a name="azkeyvault"></a>Az.KeyVault
* Aggiunta degli attributi della modifica di rilievo a 'New-AzKeyVault'

#### <a name="azmonitor"></a>Az.Monitor
* Documentazione aggiornata per 'New-AzScheduledQueryRuleLogMetricTrigger'

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento dei cmdlet per consentire VirtualHubVnetConnections tra tenant
    - 'New-AzVirtualHubVnetConnection'
    - 'Update-AzVirtualHubVnetConnection'
    - 'New-AzVirtualHub'
    - 'Update-AzVirtualHub'
* Rimozione della dipendenza di SQL Management SDK

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Miglioramento dei messaggi di errore

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery: aggiunto il supporto per la riprotezione e aggiornamento delle proprietà delle VM per le macchine virtuali con crittografia dischi di Azure.
* Azure Site Recovery: aggiunta del monitoraggio per il ripristino di emergenza nelle proprietà VmwareToAzure
* Backup di Azure: aggiunta del supporto per la ripetizione dell'aggiornamento dei criteri per gli elementi non riusciti.
* Backup di Azure: aggiunta del supporto per le impostazioni di esclusione disco durante il backup e il ripristino.
* Backup di Azure: aggiunta del supporto per il ripristino di più file/cartelle in AzureFileShare
* Backup di Azure: aggiunta del supporto per il gruppo di risorse specificato dall'utente durante l'aggiornamento dei criteri IaasVM

#### <a name="azresources"></a>Az.Resources
* Correzione di 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' per l'utilizzo del valore effettivo di apiVersion per le risorse invece di quello predefinito [#11267]
* Aggiunta della registrazione di correlationId per gli scenari di errore
* Modifica di lieve entità alla documentazione di 'Get-AzResourceLock'. Aggiunta dell'esempio.
* Aggiunta della virgoletta singola come carattere di escape nel valore di parametro 'Get-AzADUser' [#11317]
* Aggiunta di nuovi cmdlet per gli script di distribuzione ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')

#### <a name="azsql"></a>Az.Sql
* Aggiunta del parametro secondario leggibile a 'Invoke-AzSqlDatabaseFailover'
* Aggiunta del cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'
* Salvataggio della classificazione di riservatezza durante la classificazione delle colonne nel database.

#### <a name="azsupport"></a>Az.Support
* Disponibilità generale del modulo 'Az.Support'

#### <a name="azwebsites"></a>Az.Websites
* Aggiunta del supporto per l'uso delle regole di gestione del traffico delle app Web con i nuovi cmdlet seguenti
    - 'Get-AzWebAppTrafficRouting'
    - 'Update-AzWebAppTrafficRouting'
    - 'Add-AzWebAppTrafficRouting'
    - 'Remove-AzWebAppTrafficRouting'

## <a name="361---march-2020"></a>3.6.1 - Marzo 2020
#### <a name="azaccounts"></a>Az.Accounts
* Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]
* Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]
* Aggiunta la versione Az in UserAgent

#### <a name="azapimanagement"></a>Az.ApiManagement
* Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]
* 'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]
* 'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON
* 'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta del supporto per la gestione dei dispositivi in un hub IoT. I nuovi cmdlet sono:
    - 'Add-AzIotHubDevice'
    - 'Get-AzIotHubDevice'
    - 'Remove-AzIotHubDevice'
    - 'Set-AzIotHubDevice'
* Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT. I nuovi cmdlet sono:
    - 'Add-AzIotHubModule'
    - 'Get-AzIotHubModule'
    - 'Remove-AzIotHubModule'
    - 'Set-AzIotHubModule'
* Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.
* Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.
* Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT. I nuovi cmdlet sono:
    - 'Get-AzIotHubDeviceParent'
    - 'Set-AzIotHubDeviceParent'
* Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.

#### <a name="azmonitor"></a>Az.Monitor
* Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento di SQL Management SDK.
* Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.
    - Mapping del campo ActionsRequired a ActionRequired.
* Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'

#### <a name="azresources"></a>Az.Resources
* Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'
* Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]
* Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]
* Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]
* Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand
* Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri
* Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server
* Estensione dei cmdlet Tag per l'accettazione di -ResourceId
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Aggiunta di nuovi cmdlet Tag
    - Update-AzTag -ResourceId
* Inclusione di ScopedDeployment da SDK 3.3.0

#### <a name="azsql"></a>Az.Sql
* Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'
* Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti
    - Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito
    - Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione
    - Rimozione di un backup con conservazione a lungo termine
    - Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito
* Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer
* Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance
* Bump della versione di SQL SDK per Az.Network

#### <a name="azstorage"></a>Az.Storage
* Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy
    - 'Set-AzRmStorageContainerImmutabilityPolicy'
* Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura
    - 'New-AzStorageTable'
    - 'Get-AzStorageTable'

#### <a name="azwebsites"></a>Az.Websites
* Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'
* Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web
* Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app
* Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi
* Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots

## <a name="350---february-2020"></a>3.5.0 - Febbraio 2020
### <a name="highlights-since-the-last-major-release"></a>Novità rispetto all'ultima versione principale
* Aggiornamento dei dati di telemetria lato client.
* Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.
* Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.

#### <a name="azaccounts"></a>Az.Accounts
* Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client

#### <a name="azautomation"></a>Az.Automation
* Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Aggiornamento dell'SDK alla versione 7.0
* Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto

#### <a name="azcompute"></a>Az.Compute
* Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta del supporto per la gestione dei dispositivi in un hub IoT. I nuovi cmdlet sono:
    - 'Add-AzIotHubDevice'
    - 'Get-AzIotHubDevice'
    - 'Remove-AzIotHubDevice'
    - 'Set-AzIotHubDevice'

#### <a name="azkeyvault"></a>Az.KeyVault
* Correzione del testo duplicato per Add-AzKeyVaultKey.md

#### <a name="azmonitor"></a>Az.Monitor
* Correzione della descrizione del cmdlet Get-AzLog.
* Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.
    - L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).

#### <a name="aznetwork"></a>Az.Network
* Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.
* Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.
* Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.
* Supporto di criteri firewall di Azure nei firewall di rete virtuale
    - Nessun nuovo cmdlet aggiunto. Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aggiunta del supporto del ripristino come file per database SQL.

#### <a name="azresources"></a>Az.Resources
* Refactoring dei cmdlet per la distribuzione di modelli
    - Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: *-AzManagementGroupDeployment
    - Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: *-AzTenantDeployment
    - Refactoring dei cmdlet *-AzDeployment per l'uso specifico nell'ambito della sottoscrizione
    - Creazione degli alias *-AzSubscriptionDeployment per i cmdlet *-AzDeployment
* Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato
* Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.
* Rigenerazione dei file della Guida

#### <a name="azsql"></a>Az.Sql
* Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.
* Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente
* Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Aggiunta di cmdlet per il listener del gruppo di disponibilità

#### <a name="azstoragesync"></a>Az.StorageSync
* Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.

## <a name="340---february-2020"></a>3.4.0 - Febbraio 2020
### <a name="highlights-since-the-last-major-release"></a>Novità rispetto all'ultima versione principale
* Rilascio della versione iniziale 0.1.0 di Az.CosmosDB
* Aggiunta del supporto di Az.Network ConnectionMonitor V2

#### <a name="azaccounts"></a>Az.Accounts
* Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile
* Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct*** e **Set-AzApiManagementProduct**
  - Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet

#### <a name="azcompute"></a>Az.Compute
* Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.
* Aggiunta del cmdlet Update-AzDiskEncryptionSet
* Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .NET SDK alla versione 4.7.0

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Aggiunta di operazioni LIST per le risorse
* Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità

#### <a name="azhdinsight"></a>Az.HDInsight
* Correzione dell'errore di documentazione di New-AzHDInsightCluster.

#### <a name="azkeyvault"></a>Az.KeyVault
* Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.

#### <a name="aznetwork"></a>Az.Network
* Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.
* Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione
    - Aggiornamento del cmdlet New-AzFirewall:
        - Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico
        - Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'
* Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.
* Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.
* Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione
    - Nuovi cmdlet aggiunti:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Supporto della valutazione della conformità prima di determinare la risorsa da correggere
    - Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation
* Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri
* Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Supporto di Azure Site Recovery per la rimozione di un disco replicato.
* Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.

#### <a name="azresources"></a>Az.Resources
* -Scope diventato facoltativo nei cmdlet *-AzPolicyAssignment con sottoscrizione del contesto predefinita
* Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave

#### <a name="azsql"></a>Az.Sql
Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.

#### <a name="azstorage"></a>Az.Storage
* Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione
    - New-AzStorageAccount
* Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation
* Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot
* Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly

## <a name="330---january-2020"></a>3.3.0 - Gennaio 2020
#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix

#### <a name="azcdn"></a>Az.Cdn
* Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint

#### <a name="azcompute"></a>Az.Compute
* Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'
  - Ottiene il contenitore di archiviazione Edge
* Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'
  - Crea un nuovo contenitore di archiviazione Edge
* Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'
  - Rimuove il contenitore di archiviazione Edge
* Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'
  - Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge
* Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'
  - Ottiene l'account di archiviazione Edge
* Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'
  - Crea un nuovo account di archiviazione Edge
* Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'
  - Rimuove l'account di archiviazione Edge
* Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'
  - Richiama l'azione per aggiornare i dati nella condivisione
* Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'
  - Imposta le credenziali dell'account di archiviazione az databoxedge

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime
* Aggiornamento di ADF .NET SDK alla versione 4.6.0
* Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md

#### <a name="azeventhub"></a>Az.EventHub
* Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace

#### <a name="azhdinsight"></a>Az.HDInsight
* Correzione dell'errore Invoke-AzHDInsightHiveJob.md.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.
* Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.
* Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.
* Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.

#### <a name="azresources"></a>Az.Resources
* Correzione di un errore nel documento della Guida di 'Remove-AzTag'.

#### <a name="azsql"></a>Az.Sql
* Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.
* Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido

#### <a name="azstorage"></a>Az.Storage
* Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura
    - Update-AzStorageAccountNetworkRuleSet
* Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 - Dicembre 2019

### <a name="general"></a>Generale
* Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli

#### <a name="azaccounts"></a>Az.Accounts
* Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0
* Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0

#### <a name="azbatch"></a>Az.Batch
* Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .NET SDK alla versione 4.5.0

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall
* Aggiunta di SocketAddr al completamento automatico

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Gestione delle eccezioni

#### <a name="azkeyvault"></a>Az.KeyVault
* Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato
* Gestione del certificato di crittografia a curva ellittica (ECC)
    - Aggiunta del supporto per la specifica della curva per i criteri del certificato

#### <a name="azmonitor"></a>Az.Monitor
* Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica. Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia un tipo di dati dedicato)

#### <a name="aznetwork"></a>Az.Network
* Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.

#### <a name="azresources"></a>Az.Resources
* Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.
* Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.

#### <a name="azsql"></a>Az.Sql
* Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità

#### <a name="azstorage"></a>Az.Storage
* Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità
    - Revoke-AzStorageAccountUserDelegationKeys
* Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.
* Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'
    - Set-AzStorageShareQuota
* Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 - Novembre 2019
### <a name="highlights-since-the-last-major-release"></a>Novità rispetto all'ultima versione principale
* Rilascio di Az.DataBoxEdge 1.0.0
* Rilascio di Az.SqlVirtualMachine 1.0.0

#### <a name="azcompute"></a>Az.Compute
* Funzionalità Riapplica macchina virtuale
    - Aggiunta del parametro Reapply al cmdlet Set-AzVM
* Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:
    - Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss
* Supporto delle immagini della raccolta tra tenant per New-AzVM
* Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss
* Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk
* Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo
* Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion
* Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition
* Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`
    - Recupera l'ordine
* Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`
    - Crea un nuovo ordine
* Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`
    - Rimuove l'ordine
* Modifica nel cmdlet `New-AzDataBoxEdgeShare`
    - Ora crea una condivisione locale
* Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`
    - Ora è possibile mappare IotRole alla condivisione
* Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`
    - Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo
* Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`
    - Recupera le informazioni sui trigger
* Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`
    - Crea nuovi trigger
* Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`
    - Rimuove i trigger

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .NET SDK alla versione 4.4.0
* Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem

#### <a name="azeventhub"></a>Az.EventHub
* Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject
* Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject
* Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.

#### <a name="azprivatedns"></a>Az.PrivateDns
* Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.
* Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.
* Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.

#### <a name="azrediscache"></a>Az.RedisCache
* Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'. È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.
* Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'

#### <a name="azresources"></a>Az.Resources
- Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.
- Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione
- Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.
- Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.
- Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.

#### <a name="azsql"></a>Az.Sql
* Aggiunta del supporto per ReadReplicaCount per il database.
* Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata

## <a name="300---november-2019"></a>3.0.0 - Novembre 2019
### <a name="general"></a>Generale
* Rilasciato AZ. PrivateDns 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.

#### <a name="azadvisor"></a>Az.Advisor
* Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.

#### <a name="azbatch"></a>Az.Batch
* Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`. È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.
  - Questa modifica influisce su **Get-AzBatchAccount**.
* Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.
* Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`. Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.
  - Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:
    - I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.
    - I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.
* Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.
  - È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**. Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.
  - `ApplicationId` è ora un alias di `ApplicationName`.
* Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.
* Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.
* Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.
* Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.
* Rimozione di **set-AzBatchPoolOSVersion**. Questa operazione non è più supportata.
* Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.
* Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.
* Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.
* Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.
  - **Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.
  - Vengono inoltre restituite nuove immagini non verificate. Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.
* Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.
* Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico. Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.
* Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch. Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.
* Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`. Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.
* Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).
* Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).

#### <a name="azcdn"></a>Az.Cdn
* Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.
* Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.

#### <a name="azcompute"></a>Az.Compute
* Funzionalità Set di crittografia dischi
    - Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet
    - Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
    - Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig
* Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig
* Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta
* Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss
* Modifiche di rilievo
    - Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB
    - PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .NET SDK alla versione 4.3.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti
* Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.
* Esposizione dell'impostazione per timeout della richiesta in adlsclient
* Correzione del passaggio di syncflag originale per il ripristino di badoffset
* Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta
* Correzione del bug Concat

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Correzione di vari errori di ortografia nei moduli

#### <a name="azhdinsight"></a>Az.HDInsight
* Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.
* Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.
* Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0
* Rimozione di cinque cmdlet:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Aggiunta di tre cmdlet:
    - Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.
    - Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.
    - Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.
* Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.
* Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.
* Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.
* Modifica del tipo di output per i cmdlet seguenti:
*  - Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.
*  - Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.
*  - Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.
* Aggiunta di alcuni test case dello scenario.
* Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.

#### <a name="aziothub"></a>Az.IotHub
* Modifiche di rilievo:
    - Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.
    - Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.
    - Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.
    - Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.
    - La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.
    - La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.
    - Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.
    - Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.
    - Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.
    - Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.
    - Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.
    - Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.
* Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.
* Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.
* Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.
* Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.
* Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.
* Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.
* Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.
* Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete

#### <a name="azresources"></a>Az.Resources
* Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2

#### <a name="aznetwork"></a>Az.Network
* Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.
    - Cmdlet aggiornato:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.
    - Nuovo cmdlet:
        - Get-AzPrivateLinkResource
* Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.
    - Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService
    - Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection
    - Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.
* Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'
* Nuovi cmdlet per il supporto dei criteri firewall di Azure
* Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub
    - Nuovi cmdlet aggiunti:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan
    - Aggiornamento di cmdlet con parametri facoltativi:
        - New-AzVirtualHub: aggiunta del parametro Sku
        - Update-AzVirtualHub: aggiunta del parametro Sku
        - New-AzVirtualWan: aggiunta del parametro VirtualWANType
        - Update-AzVirtualWan: aggiunta del parametro VirtualWANType
* Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection
    - Nuovi cmdlet aggiunti:
        - Update-AzureRmVirtualHubVnetConnection
    - Aggiornamento di cmdlet con parametri facoltativi:
        - New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity
        - New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity
        - Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity
        - New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity
        - Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity
* Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall
    - Nuovi cmdlet aggiunti:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Aggiornamento di cmdlet con parametri facoltativi:
        - New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule
* Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule
    - Aggiunta di GeoMatch all'operatore in FirewallCondition
* Aggiunta del supporto per i criteri firewall perListener e perSite
    - Aggiornamento di cmdlet con parametri facoltativi:
        - New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId
        - New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId
* Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole
* Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure
* Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup
    - Nuovi cmdlet aggiunti:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.

#### <a name="azsql"></a>Az.Sql
* Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.
* Deprecazione dei vecchi cmdlet di controllo dal codice.
* Rimozione di alias deprecati:
* Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)
* Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)
* Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati
* Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato
* Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.

#### <a name="azstorage"></a>Az.Storage
* Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

## <a name="280---october-2019"></a>2.8.0 - ottobre 2019
### <a name="general"></a>Generale
* Az.HealthcareApis 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet
    - correzione del problema https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.

#### <a name="azbatch"></a>Az.Batch
* **Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.

#### <a name="azcompute"></a>Az.Compute
* Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss
* Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey
* Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.
* Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.
* Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.
* Aggiornamento di ADF .NET SDK alla versione 4.2.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Aggiornamento di PowerShell alla versione 1.0.0
* Aggiornamento dell'SDK alla versione 1.0.2
* Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK
* Aggiornamento della struttura dell'output da annidata ad appiattita.

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents
* Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId

#### <a name="azmonitor"></a>Az.Monitor
* Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Uso dello schema di avviso comune abilitato per i ricevitori. Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT
* I webhook supportano ora l'autenticazione di Azure Active Directory.

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.
* Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale
    - Nuovi cmdlet aggiunti:
        - New-AzureRmTrafficSelectorPolicy
    - Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
* Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete
    - Aggiornamento dei cmdlet:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Miglioramento della gestione delle eccezioni nei cmdlet Cortex
* Nuove generazioni e SKU per VirtualNetworkGateways
  - Introduzione di nuove generazioni per VirtualNetworkGateways.
  - Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.

#### <a name="azrediscache"></a>Az.RedisCache
* Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"

#### <a name="azsql"></a>Az.Sql
* Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita

#### <a name="azstorage"></a>Az.Storage
* Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0
* Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink
    -  Get-AzRmStorageContainer
* Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito

## <a name="270---september-2019"></a>2.7.0 - Settembre 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'
* Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento. Usare invece 'set-AzApiManagement'.

#### <a name="azautomation"></a>Az.Automation
* Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'
* Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode
* Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.

#### <a name="azcompute"></a>Az.Compute
* Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig
* Aggiunta del parametro Incremental a New-AzSnapshotConfig
* Aggiunta di una funzionalità di macchina virtuale a priorità bassa:
    - Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.
    - Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.
* Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.
* Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.
* Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.
* Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus
* Aggiornamento di ADF .NET SDK alla versione 4.1.3

#### <a name="azhdinsight"></a>Az.HDInsight
* Modifiche di rilievo

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.
* Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT. I nuovi cmdlet sono:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)
   - Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit. Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.
   - La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**. I test dello scenario sono stati aggiornati per riflettere questa modifica.
   - Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**. Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet. **NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.
   - L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente. Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.
   - L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente. Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.
* Supporto dei criteri di soglia dinamica per l'avviso della metrica V2
    - New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica
    - Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica
* Miglioramenti dei cmdlet Scheduled Query Rule (SQR)
 - I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)
 - Descrizione corretta del parametro 'Enabled' nei file della Guida
 - Aggiunta di esempi per il parametro facoltativo 'ActionGroup'
 - Miglioramento generale dei file della Guida
* Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'

#### <a name="aznetwork"></a>Az.Network
* Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'
* Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto
* Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete
* Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti
* Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK
* Correzione del mapping errato di modelli di regole di sicurezza
* Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato
    - Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface
    - Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration
    - Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation
* Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure
* Supporto di MultiLink nella rete WAN virtuale
    - Nuovi cmdlet
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Cmdlet aggiornato:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount
* Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale

#### <a name="azresources"></a>Az.Resources
* Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'
* Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.

#### <a name="azsignalr"></a>Az.SignalR
* Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage

#### <a name="azsql"></a>Az.Sql
* Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'
* Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).
* Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy
* Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.
* Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'
* Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.
    -  Set-AzStorageBlobContent
* Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP
* Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows
* Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'

## <a name="260---august-2019"></a>2.6.0 - Agosto 2019
#### <a name="general"></a>Generale
* Correzione di vari errori di ortografia in numerosi moduli

#### <a name="azaccounts"></a>Az.Accounts
* Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)

#### <a name="azaks"></a>Az.Aks
* Correzione del problema relativo all'output di 'Get-AzAks'
    * Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* correzione del problema https://github.com/Azure/azure-powershell/issues/9351
    - Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId
* **Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752
* Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'

#### <a name="azbatch"></a>Az.Batch
* Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola

#### <a name="azcdn"></a>Az.Cdn
* Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN

#### <a name="azcompute"></a>Az.Compute
* Aggiunta di VmssId al cmdlet New-AzVMConfig
* Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss
* Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale
* Aggiunta delle funzionalità Host e HostGroup
    - Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM
* Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto
* Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'

#### <a name="azdatafactory"></a>Az.DataFactory
* Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola
* Aggiornamento di ADF .NET SDK alla versione 4.1.2
* Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime
* Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.

#### <a name="azeventhub"></a>Az.EventHub
* Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet
* Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace
* Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace
* Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo

#### <a name="azmonitor"></a>Az.Monitor
* Correzione del nome di parametro errato nella documentazione della Guida

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento di New-AzPrivateLinkServiceIpConfig
    - Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.
    - Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.
* Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati
* Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.
* Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.
* Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'
    - Aggiunta dell'esempio
    - Aggiornamento della descrizione per il parametro '-Name'
* Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource
* Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'

#### <a name="azresources"></a>Az.Resources
* Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource
    - Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà
    - Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa
* Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida

#### <a name="azservicebus"></a>Az.ServiceBus
* Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet
* Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto
* Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correzione dei bug del cmdlet di aggiunta del tipo di nodo:
    - bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric. Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681
    - Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster. Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407
    - Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate

#### <a name="azsql"></a>Az.Sql
* Aggiornamento della documentazione dei vecchi cmdlet Auditing.

#### <a name="azstorage"></a>Az.Storage
* Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento
* Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Supporto di Priorità di riattivazione nell'operazione di copia BLOB
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot

## <a name="250---july-2019"></a>2.5.0 - Luglio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'

#### <a name="azautomation"></a>Az.Automation
* Correzione dell'errore di ortografia nella stringa di risorsa

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Aggiunta del supporto per NetworkRuleSet.

#### <a name="azcompute"></a>Az.Compute
* Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication
    - Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento di ADF .NET SDK alla versione 4.1.0
* Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'

#### <a name="azeventhub"></a>Az.EventHub
* Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken
* Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'

#### <a name="azkeyvault"></a>Az.KeyVault
* Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati

#### <a name="azlogicapp"></a>Az.LogicApp
* Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping
    - Aggiunta del nuovo parametro MapType per il filtro

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato
    - Nuovi cmdlet
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork
    - Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig
        - Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.
        - Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.
* Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti
* Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete
    - Aggiornamento dei cmdlet:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection
* Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration
    - Cmdlet aggiornato:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe
    - Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end. Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Aggiornamento della versione predefinita per le versioni salvate su 1.
* Correzione della gestione delle espressioni regolari Null di log personalizzati

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'
* Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'
* Aggiornamento di 'Get-AzRecoveryServicesVault.md'
* Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'
* Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'
* Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'
* Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'
* Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'
* Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure
* Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'

#### <a name="azresources"></a>Az.Resources
- Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'
- Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01

#### <a name="azservicebus"></a>Az.ServiceBus
* Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken
* Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'

#### <a name="azsql"></a>Az.Sql
* Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary
* Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica
* Correzione di un errore di ortografia in un messaggio di avviso.

#### <a name="azstorage"></a>Az.Storage
* Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto

#### <a name="azstoragesync"></a>Az.StorageSync
* Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.
* Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays

#### <a name="azwebsites"></a>Az.Websites
* Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp
* Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp
* Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots

## <a name="240---july-2019"></a>2.4.0 - Luglio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiunta del supporto per i cmdlet del profilo
* Aggiunta del supporto per ambienti e piani dati nei cmdlet generati
* Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell

#### <a name="azadvisor"></a>Az.Advisor
* Versione in disponibilità generale di Az.Advisor
* Questo modulo è ora incluso come parte del modulo `Az` di rollup

#### <a name="azapimanagement"></a>Az.ApiManagement
* correzione del problema https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto
        - Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'
* Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API

#### <a name="azautomation"></a>Az.Automation
* Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.

#### <a name="azcompute"></a>Az.Compute
* Aggiunta del parametro HyperVGeneration a New-AzImageConfig

#### <a name="azdatafactory"></a>Az.DataFactory
* Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.

#### <a name="azeventgrid"></a>Az.EventGrid
* Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'

#### <a name="aziothub"></a>Az.IotHub
* Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.

#### <a name="aznetwork"></a>Az.Network
* Aggiunta di 'RoutingPreference' ai tag degli IP pubblici
* Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Correzione del problema relativo al riferimento Null in Get-AzPolicyState
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Correzione del comando get-policy per le VM IaaS

#### <a name="azresources"></a>Az.Resources
    - Correzione del testo della Guida per il parametro Get-AzPolicyState -Top
    - Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias
    - Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject
    - Aggiornamento di documentazione ed esempi per i cmdlet Policy

#### <a name="azservicebus"></a>Az.ServiceBus
* Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes

#### <a name="azsql"></a>Az.Sql
* Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica
* Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità

#### <a name="azstorage"></a>Az.Storage
* Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:
    -  Enable-AzStorageStaticWebsite
* Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio
* Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException
* Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Questo modulo è ora incluso come parte del modulo `Az` di rollup

## <a name="232---june-2019"></a>2.3.2 - giugno 2019
#### <a name="azaccounts"></a>Az.Accounts
* Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni
    - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983
* Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.
* Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'

#### <a name="azdns"></a>Az.Dns
* Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.

#### <a name="azeventgrid"></a>Az.EventGrid
* Aggiornamento per l'uso della versione dell'API 2019-06-01.
* Nuovi cmdlet:
    - New-AzureRmEventGridDomain
        - Crea un nuovo dominio di Griglia di eventi di Azure.
    - Get-AzureRmEventGridDomain
        - Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.
    - Remove-AzureRmEventGridDomain
        - Rimuove un dominio di Griglia di eventi di Azure.
    - New-AzureRmEventGridDomainKey
        - Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.
    - Get-AzureRmEventGridDomainKey
        - Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.
    - New-AzureRmEventGridDomainTopic:
        - Crea un nuovo dominio di Griglia di eventi di Azure.
    - Get-AzureRmEventGridDomainTopic
        - Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.
    - Remove-AzureRmEventGridDomainTopic
        - Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.
* Aggiornamento dei cmdlet:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription
        - Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.
        - Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.
        - Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.
        - aggiunta di nuovi parametri facoltativi che consentono di specificare:
            - Data di scadenza della sottoscrizione di eventi
            - Parametri di filtro avanzati.
        - Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.
        - Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription
        - Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.
    - Remove-AzureRmEventGridSubscription
        - Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.
        - Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)
* New-AzFrontDoorWafManagedRuleObject
    - Aggiunta di nuovi valori per il completamento automatico

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del supporto per la risorsa gateway di rete virtuale
    - Nuovi cmdlet
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Aggiunta di AvailablePrivateEndpointType
    - Nuovi cmdlet
        - Get-AzAvailablePrivateEndpointType
* Aggiunta di PrivatePrivateLinkService
    - Nuovi cmdlet
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Aggiunta di PrivateEndpoint
    - Nuovi cmdlet
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection
    - Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.
    - Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.
* Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.
* Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.
* Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit
* Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration
* Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.
* Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration
* Correzione dei cmdlet Get di Cortex per la parte list all
* Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway
* Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway
* Aggiunta del cmdlet Get-AzNetworkServiceTag
* Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure
    - Aggiornamento del cmdlet New-AzFirewall:
        - Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico
        - Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale
        - Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico
        - Parametri deprecati: -PublicIpName e -VirtualNetworkName
* Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.
    - Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.
    - Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.
    - Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'

#### <a name="azresources"></a>Az.Resources
* Supporto per opzioni aggiuntive di esportazione modelli
    - Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup
    - Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup
    - Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata

#### <a name="azsql"></a>Az.Sql
* Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection
* Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection
* Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione
    - New-AzStorageAccount
* Descrizione del cmdlet di immutabilità BLOB più chiara
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client
* Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot

## <a name="220---june-2019"></a>2.2.0 - giugno 2019
#### <a name="azcdn"></a>Az.Cdn
* I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.

#### <a name="azcompute"></a>Az.Compute
* È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.
    - Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag
* Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName

#### <a name="aznetwork"></a>Az.Network
* Aggiornamento di ResourceId e InputObject per il gateway NAT
    - Aggiunta dell'alias per ResourceId e InputObject

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM

#### <a name="azservicebus"></a>Az.ServiceBus
* Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'
* Correzione del carattere mancante nelle righe di comando di Service Fabric

#### <a name="azsql"></a>Az.Sql
* Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.
* Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection
* I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.

#### <a name="azwebsites"></a>Az.Websites
* Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi

## <a name="210---may-2019"></a>2.1.0 - maggio 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API
    - **Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API
    - **New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API
    - **New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo
    - **New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.
    - **New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica
    - **Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API
    - **Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API
* Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement
    - **Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache
    - **New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure
    - **Remove-AzApiManagementCache**: rimuove una cache
    - **Update-AzApiManagementCache**: aggiorna una cache
* Creazione di nuovi cmdlet per la gestione dello schema dell'API
    - **New-AzApiManagementSchema**: crea un nuovo schema per un'API
    - **Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API
    - **Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API
    - **Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API
* Creazione di un nuovo cmdlet per la generazione di un token utente.
    - **New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.
* Creazione di un nuovo cmdlet per il recupero dello stato della rete
    - **Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement. È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.
* Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement
    - Aggiunta del supporto per il nuovo SKU 'Consumption'
    - Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'
    - Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'. Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.
    - Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.
* Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'
* Aggiornamento del cmdlet per visualizzare i messaggi di errore inline
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]
* Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'
* Aggiornamento del cmdlet **Import-AzApiManagementApi**
    - Per importare l'API dalla specifica del documento 'OpenApi 3.0'
    - Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').
    - Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.
* Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'
* Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'
* Aggiornamento del cmdlet **New-AzApiManagementApi**
    - Per configurare l'API con il server di autorizzazione 'OpenId'.
    - Per creare un'API in un'interfaccia 'ApiVersionSet'
    - Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.
    - Possibilità di configurare 'SubscriptionRequired' a livello di API.
* Aggiornamento del cmdlet **Set-AzApiManagementApi**
    - Per configurare l'API con il server di autorizzazione 'OpenId'.
    - Per aggiornare un'API in un'interfaccia 'ApiVersionSet'
    - Possibilità di configurare 'SubscriptionRequired' a livello di API.
* Aggiornamento del cmdlet **New-AzApiManagementRevision**
    - Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'. La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.
    - Per fornire un oggetto 'ApiRevisionDescription'
    - Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.
* Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**
    - Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'
    - Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'
* Aggiornamento del cmdlet **New-AzApiManagementSubscription**
    - Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'
    - Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'
    - Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.
* Aggiornamento del cmdlet **Set-AzApiManagementSubscription**
    - Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'
    - Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'
    - Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.
* Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'
    - 'New-AzApiManagementContext'
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - 'Get-AzApiManagementApiRelease'
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - 'Get-AzApiManagementApiVersionSet'
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - 'Get-AzApiManagementAuthorizationServer'
    - 'Get-AzApiManagementBackend'
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - 'Get-AzApiManagementCertificate'
    - 'Remove-AzApiManagementApiVersionSet'
    - 'Remove-AzApiManagementSubscription'

#### <a name="azautomation"></a>Az.Automation
* Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.
    - correzione del problema https://github.com/Azure/azure-powershell/issues/7977
    - correzione del problema https://github.com/Azure/azure-powershell/issues/8600
* Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.
    * correzione del problema https://github.com/Azure/azure-powershell/issues/8347
* Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name. Ora viene restituito solo il nodo corrispondente.

#### <a name="azcompute"></a>Az.Compute
* Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.
* Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure

#### <a name="azmonitor"></a>Az.Monitor
* Correzione dei nomi di parametri errati negli esempi della Guida

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva
    - Cmdlet aggiornato:
        - Get-AzEffectiveRouteTable
* Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate

#### <a name="azresources"></a>Az.Resources
* Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto

#### <a name="azsql"></a>Az.Sql
* Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita

## <a name="200---may-2019"></a>2.0.0 - Maggio 2019
#### <a name="azaccounts"></a>Az.Accounts
* Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.
* Miglioramento dell'errore quando la creazione dell'account non riesce.

#### <a name="azcompute"></a>Az.Compute
* Funzionalità Gruppo di selezione host di prossimità.
    - Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.
* TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.
* Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss
* Modifiche di rilievo
    - Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.
    - Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager

#### <a name="azdns"></a>Az.Dns
* Delega automatica del server dei nomi DNS
    - Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.
    - Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure
* Ridenominazione dei cmdlet WAF in modo da includere 'Waf'
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Rimozione di due cmdlet:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess
* Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:
    - Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.
    - Gli utenti con ruolo di operatore hdinsight non sono interessati.

#### <a name="azmonitor"></a>Az.Monitor
* Nuovi cmdlet per l'API SQR (regola di query pianificata)
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR
    - Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)

#### <a name="aznetwork"></a>Az.Network
* Aggiunta del supporto per la risorsa gateway NAT
    - Nuovi cmdlet
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Aggiornamento dei cmdlet:
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.
    - Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.
    - Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Supporto per eseguire query sui dettagli di valutazione dei criteri.
    - Aggiunta del parametro '-Expand' a Get-AzPolicyState. Supporto di '-Expand PolicyEvaluationDetails'.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.
* Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.
* Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.
* Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.
* Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.
* Altre correzioni minori.

#### <a name="azrelay"></a>Az.Relay
* Correzione di errori ortografici in messaggi per i clienti

#### <a name="azservicebus"></a>Az.ServiceBus
* Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi

#### <a name="azstorage"></a>Az.Storage
* Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')
* Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.
* Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'
    - New-AzStorageAccount
* L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp
* Get-AzWebApp*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati

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
