---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 563f84c3af98de066611dd80102e552b31f12883
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2018
ms.locfileid: "52827140"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

## <a name="20170925---version-440"></a>25.09.2017 - Versione 4.4.0
* AnalysisServices
  * Aggiunta di un nuovo cmdlet dataplane per consentire la sincronizzazione dei database dall'istanza di lettura/scrittura a istanze di sola lettura
    - File della Guida inclusi per il cmdlet
    - Aggiunta di test delle funzionalità in memoria e di uno scenario di test (solo live)
  * Correzione di bug nel cmdlet Add-AzureAsAccount
* Automazione
  * Correzione di documenti della Guida per i cmdlet corretti nella versione precedente.
  * Aggiunta di 4 nuovi cmdlet per l'implementazione in fasi di configurazioni del nodo DSC.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Integrazione con Cognitive Services Management SDK versione 2.0.0.
  * Get-AzureRmCognitiveServicesAccount supporta ora correttamente il paging.
* Calcolo
  * Funzionalità dei comandi di esecuzione:
    - Il nuovo cmdlet: 'Invoke-AzureRmVMRunCommand' richiama un comando di esecuzione in una macchina virtuale
    - Il nuovo cmdlet: 'Get-AzureRmVMRunCommandDocument' visualizza i documenti disponibili per i comandi di esecuzione
  * Aggiunta del parametro 'StorageAccountType' a Set-AzureRmDataDisk
  * Supporto delle zone di disponibilità per macchine virtuali, set di scalabilità di macchine virtuali e dischi
    - Aggiunta del nuovo parametro: 'Zone' a New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig
  * Funzionalità di aggiornamento in sequenza dei set di scalabilità di macchine virtuali:
    - Il nuovo cmdlet: 'Start-AzureRmVmssRollingOSUpgrade' richiama l'aggiornamento in sequenza del sistema operativo del set di scalabilità di macchine virtuali
    - Il nuovo cmdlet: 'Set-AzureRmVmssRollingUpgradePolicy' imposta i criteri di aggiornamento in sequenza del set di scalabilità di macchine virtuali.
    - Il nuovo cmdlet: 'Stop-AzureRmVmssRollingUpgrade' annulla l'aggiornamento in sequenza del set di scalabilità di macchine virtuali
    - Il nuovo cmdlet: 'Get-AzureRmVmssRollingUpgrade' visualizza lo stato dell'aggiornamento in sequenza del set di scalabilità di macchine virtuali.
  * È stato introdotto il parametro opzionale AssignIdentity per l'identità assegnata dal sistema.
    - Aggiunta del nuovo parametro: 'AssignIdentity' a New-AzureRmVMConfig, New-AzureRmVmssConfig e Update-AzureRmVM
  * Funzionalità di crittografia dei dischi di set di scalabilità di macchine virtuali:
    - Il nuovo cmdlet: 'Set-AzureRmVmssDiskEncryptionExtension' abilita la crittografia del disco nel set di scalabilità di macchine virtuali
    - Il nuovo cmdlet: 'Disable-AzureRmVmssDiskEncryption' disabilita la crittografia del disco nel set di scalabilità di macchine virtuali
    - Il nuovo cmdlet: 'Get-AzureRmVmssDiskEncryptionStatus' visualizza lo stato di crittografia del disco di un set di scalabilità di macchine virtuali
    - Il nuovo cmdlet: 'Get-AzureRmVmssVMDiskEncryptionStatus' visualizza lo stato di crittografia del disco di una VM in un set di scalabilità di macchine virtuali
* ContainerInstance
  * Aggiunta di cmdlet PowerShell per Istanze di contenitore di Azure
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Informazioni dettagliate
  * Nuovo cmdlet Disable-AzureRmActivityLogAlert
    - Nuovo cmdlet per disabilitare un avviso esistente del log attività.
    - È possibile impostare anche i tag con questo cmdlet.
  * Nuovo cmdlet Enable-AzureRmActivityLogAlert
    - Nuovo cmdlet per abilitare un avviso esistente del log attività.
    - È possibile impostare anche i tag con questo cmdlet.
  * Nuovo cmdlet Get-AzureRmActivityLogAlert
    - Nuovo cmdlet per recuperare uno o più avvisi del log attività.
    - Gli avvisi possono essere recuperati per nome, gruppo di risorse o sottoscrizione.
  * Nuovo cmdlet New-AzureRmActionGroup
    - Nuovo cmdlet per creare un oggetto ActionGroup in memoria (senza richiesta).
  * Nuovo cmdlet New-AzureRmActivityLogAlertCondition
    - Nuovo cmdlet per la creazione di un oggetto di condizione foglia per avvisi del registro attività in memoria (senza richiesta).
  * Nuovo cmdlet Set-AzureRmActivityLogAlert
    - Nuovo cmdlet per creare o aggiornare un avviso del log attività.
  * Nuovo cmdlet Remove-AzureRmActivityLogAlert
    - Nuovo cmdlet per rimuovere un avviso del log attività.
  * Nuovo cmdlet Set-AzureRmActionGroup
    - Nuovo cmdlet per creare un nuovo gruppo di azioni o aggiornarne uno esistente.
  * Nuovo cmdlet Get-AzureRmActionGroup
    - Nuovo cmdlet per recuperare uno o più gruppi di azioni.
    - I gruppi di azioni possono essere recuperati per nome, gruppo di risorse o sottoscrizione.
  * Nuovo cmdlet Remove-AzureRmActionGroup
    - Nuovo cmdlet per rimuovere un gruppo di azioni.
  * Nuovo cmdlet New-AzureRmActionGroupReceiver
    - Nuovo cmdlet per creare un nuovo ricevitore del gruppo di azioni in memoria.
* Insieme di credenziali delle chiavi
  * Cmdlet nuovi/aggiornati per supportare l'eliminazione temporanea per i certificati dell'insieme di credenziali delle chiavi
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Rete
  * Aggiunta del supporto per i servizi di endpoint alle subnet di rete virtuale
    - Aggiornamento di Add-AzureRmVirtualSubnetConfig: aggiunta del parametro facoltativo -ServiceEndpoint
    - Aggiornamento di New-AzureRmVirtualSubnetConfig: aggiunta del parametro facoltativo -ServiceEndpoint
    - Aggiornamento di Set-AzureRmVirtualSubnetConfig: aggiunta del parametro facoltativo -ServiceEndpoint
  * Aggiunta di un cmdlet per elencare i servizi di endpoint disponibili nella posizione
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Aggiunta della possibilità di configurare l'autenticazione da punto a sito basata su server RADIUS esterno ai cmdlet seguenti
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Aggiunta di un cmdlet per consentire la generazione di profili VPN per l'autenticazione da punto a sito basata su server RADIUS esterno
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Aggiunta del supporto per il parametro SKU agli indirizzi IP pubblici e ai servizi di bilanciamento del carico
    - Aggiornamento di New-AzureRMLoadBalancer: aggiunta del parametro facoltativo -Sku
    - Aggiornamento di New-AzureRMPublicIpAddress: aggiunta del parametro facoltativo -Sku
  * Aggiunta del supporto per DisableOutboundSNAT alle regole del servizio di bilanciamento del carico
    - Aggiornamento di New-AzureRMLoadBalancerRuleConfig: aggiunta del parametro facoltativo DisableOutboundSNAT
    - Aggiornamento di Add-AzureRMLoadBalancerRuleConfig: aggiunta del parametro facoltativo DisableOutboundSNAT
    - Aggiornamento di Set-AzureRMLoadBalancerRuleConfig: aggiunta del parametro facoltativo DisableOutboundSNAT
  * Aggiunta del supporto di IkeV2 da punto a sito
    - Aggiornamento di New-AzureRmVirtualNetworkGateway: aggiunta del parametro facoltativo -VpnClientProtocol, con valore predefinito [ "SSTP", "IkeV2" ]
    - Aggiornamento di Set-AzureRmVirtualNetworkGateway: aggiunta del parametro facoltativo -VpnClientProtocol
  * Aggiunta del supporto per le regole multivalore nelle regole di sicurezza di rete e nelle regole di sicurezza di rete effettive
    - Aggiornamento di Add-AzureRmNetworkSecurityRuleConfig: aggiornamento dei parametri SourcePortRange, DestinationPortRange, SourceAddressPrefix per l'accettazione di un elenco di stringhe
    - Aggiornamento di New-AzureRmNetworkSecurityRuleConfig: aggiornamento dei parametri SourcePortRange, DestinationPortRange, SourceAddressPrefix per l'accettazione di un elenco di stringhe
    - Aggiornamento di Set-AzureRmNetworkSecurityRuleConfig: aggiornamento dei parametri SourcePortRange, DestinationPortRange, SourceAddressPrefix per l'accettazione di un elenco di stringhe
    - Aggiornamento di Add-AzureRmNetworkSecurityRuleConfig: aggiornamento dei parametri SourcePortRange, DestinationPortRange, SourceAddressPrefix per l'accettazione di un elenco di stringhe
    - Aggiornamento di New-AzureRmNetworkSecurityGroup: aggiornamento dei parametri SecurityRules per l'accettazione dei parametri SourcePortRange, DestinationPortRange, SourceAddressPrefix che rappresentano elenchi di stringhe nell'oggetto PSSecurityRule
    - Aggiornamento di Get-AzureRmEffectiveNetworkSecurityGroup: aggiunta del parametro TagMap
    - Aggiornamento di Get-AzureRmEffectiveNetworkSecurityGroup: aggiornamento dell'oggetto PSEffectiveSecurityRule restituito con i parametri SourcePortRange, DestinationPortRange, SourceAddressPrefix che rappresentano elenchi di stringhe.
  * Aggiunta del supporto per la protezione DDoS per le reti virtuali
    - Aggiornamento di New-AzureRmVirtualNetwork: aggiunta dei parametri opzionali EnableDDoSProtection e EnableVmProtection
    - Aggiunta delle proprietà EnableDDoSProtection e EnableVmProtection nell'oggetto PSVirtualNetwork
  * Aggiunta del supporto per bilanciamento del carico interno a disponibilità elevata
    - Aggiornamento di Add-AzureRmLoadBalancerRuleConfig: aggiunta di All come valore accettabile per il parametro Protocol
    - Aggiornamento di New-AzureRmLoadBalancerRuleConfig: aggiunta di All come valore accettabile per il parametro Protocol
    - Aggiornamento di Set-AzureRmLoadBalancerRuleConfig: aggiunta di All come valore accettabile per il parametro Protocol
  * Aggiunta del supporto per gruppi di sicurezza delle applicazioni
    - Aggiunta di New-AzureRmApplicationSecurityGroup
    - Aggiunta di Get-AzureRmApplicationSecurityGroup
    - Aggiunta di Remove-AzureRmApplicationSecurityGroup
    - Aggiornamento di New-AzureRmNetworkInterface: aggiunta dei parametri facoltativi ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Aggiornamento di New-AzureRmNetworkInterfaceIpConfig: aggiunta dei parametri facoltativi ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Aggiornamento di Add-AzureRmNetworkInterfaceIpConfig: aggiunta dei parametri facoltativi ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Aggiornamento di Set-AzureRmNetworkInterfaceIpConfig: aggiunta dei parametri facoltativi ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Aggiornamento di New-AzureRmNetworkSecurityRuleConfig: aggiunta dei parametri facoltativi SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup e DestinationApplicationSecurityGroupId
    - Aggiornamento di Add-AzureRmNetworkSecurityRuleConfig: aggiunta dei parametri facoltativi SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup e DestinationApplicationSecurityGroupId
    - Aggiornamento di Set-AzureRmNetworkSecurityRuleConfig: aggiunta dei parametri facoltativi SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup e DestinationApplicationSecurityGroupId
  * Aggiunta di nuovi comandi per gli script VpnDeviceConfiguration
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profilo
  * Supporto di Start-Job per i cmdlet AzureRm.
    * Aggiunta del parametro -AzureRmContext per tutti i cmdlet AzureRm, con la possibilità di accettare un contesto (output di un cmdlet Context).
      - Modello comune per i processi con persistenza di contesto DISABILITATA:`Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Modello comune per i processi con persistenza di contesto ABILITATA:`Start-Job {New-AzureRmVM [... other parameters]}`
  * Rendere persistenti le informazioni di accesso tra le sessioni, nuovi cmdlet:
    - Enable-AzureRmContextAutosave: abilitare la persistenza delle credenziali di accesso tra le sessioni.
    - Disable-AzureRmContextAutosave: disabilitare la persistenza delle credenziali di accesso tra le sessioni.
  * Gestire le informazioni di contesto, nuovi cmdlet
    - Select-AzureRmContext: selezionare il contesto attivo denominato.
    - Rename-AzureRmContext: rinominare un contesto esistente per riferimento.
    - Remove-AzureRmContext: rimuovere un contesto esistente.
    - Remove-AzureRmAccount: rimuovere tutte le credenziali, le sottoscrizioni e i tenant associati a un account.
  * Gestire le informazioni di contesto, modifiche ai cmdlet:
    - Aggiunta di Scope = (Process | CurrentUser) a tutti i cmdlet per la modifica delle credenziali
    - Get-AzureRmContext: aggiunta del parametro ListAvailable per elencare tutti i contesti salvati
* Risorse
  * Aggiunta dei cmdlet PolicySetDefinition
    - Cmdlet New-AzureRmPolicySetDefinition per creare una definizione di set di criteri
    - Cmdlet Get-AzureRmPolicySetDefinition per elencare tutte le definizioni di set di criteri oppure ottenere una definizione di set di criteri specifica
    - Cmdlet Remove-AzureRmPolicySetDefinition per eliminare una definizione di set di criteri
    - Cmdlet Set-AzureRmPolicySetDefinition per aggiornare una definizione di set di criteri esistente
  * Aggiunta dei parametri -PolicySetDefinition, -Sku e -NotScope ai cmdlet New-AzureRmPolicyAssignment e Set-AzureRmPolicyAssignment
  * Aggiunta del supporto per passare l'URL del criterio ai cmdlet New-AzureRmPolicyDefinition e Set-AzureRmPolicyDefinition
  * Aggiunta del parametro -Mode al cmdlet New-AzureRmPolicyDefinition
  * Aggiunta del supporto per la rimozione dell'assegnazione ruolo tramite l'oggetto PSRoleAssignment
    - Gli utenti possono ora usare l'oggetto di input PSRoleassignmnet con il cmdlet Remove-AzureRMRoleAssignment per rimuovere l'assegnazione ruolo.
  * Aggiunta di cmdlet ManagedApplication
    - Cmdlet New-AzureRmManagedApplication per la creazione di un'applicazione gestita
    - Cmdlet Get-AzureRmManagedApplication per elencare tutte le applicazioni gestite in una sottoscrizione o per ottenere un'applicazione gestita specifica
    - Cmdlet Remove-AzureRmManagedApplication per l'eliminazione di un'applicazione gestita
    - Cmdlet Set-AzureRmManagedApplication per l'aggiornamento di un'applicazione gestita esistente
  * Aggiunta di cmdlet ManagedApplicationDefinition
    - Cmdlet New-AzureRmManagedApplicationDefinition per la creazione di una definizione di applicazione oppure tramite i file JSON mainTemplate e createUiDefinition
    - Cmdlet Get-AzureRmManagedApplicationDefinition per elencare tutte le definizioni di applicazioni gestite in un gruppo di risorse oppure per ottenere una definizione di applicazione gestita specifica
    - Cmdlet Remove-AzureRmManagedApplicationDefinition per l'eliminazione di una definizione di applicazione gestita
    - Cmdlet Set-AzureRmManagedApplicationDefinition per l'aggiornamento di una definizione di applicazione gestita esistente
* Sql
  * Aggiunta del supporto per le regole della rete virtuale
    - Aggiunta del cmdlet Get-AzureRmSqlServerVirtualNetworkRule per ottenere le regole della rete virtuale in base a un nome regola specifico oppure un elenco di regole della rete virtuale in un server di Azure SQL.
    - Aggiunta del cmdlet Set-AzureRmSqlServerVirtualNetworkRule per modificare la rete virtuale alla quale punta la regola.
    - Aggiunta del cmdlet Remove-AzureRmSqlServerVirtualNetworkRule per rimuovere una regola della rete virtuale per un server di Azure SQL.
    - Aggiunta del cmdlet New-AzureRmSqlServerVirtualNetworkRule per creare una nuova regola della rete virtuale per un server di Azure SQL.
* Siti Web
  * Aggiunta del livello PremiumV2 per i piani di servizio app
* Azure.Storage
  * Eseguire l'aggiornamento ad Azure Storage Client Library 8.4.0 e Azure Storage DataMovement Library 0.6.1
  * Aggiunta del supporto di PremiumPageBlobTier nell'API di copia e caricamento BLOB
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Ridefinizione del formato di output console di AzureStorageContainer, AzureStorageBlob, AzureStorageQueue e AzureStorageTable
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>10.08.2017 - Versione 4.3.1
  * Aggiornamento per risolvere il problema di firma dell'assembly

## <a name="20170807---version-430"></a>07.08.2017 - Versione 4.3.0
* AnalysisServices
  * Correzione del bug in Set-AzureRmAnalysisServicesServer
    - Quando l'amministratore non viene specificato, l'amministratore viene rimosso.
  * Aggiunta di Added BackupBlobContainerUri in New-AzureRmAnalysisServicesServer e Set-AzureRmAnalysisServicesServer
    - Possibilità di impostare o disabilitare il contenitore BLOB di backup per backup e ripristino del server di Azure Analysis Services
  * Aggiornamento della ricerca di SKU in New-AzureRmAnalysisServicesServer e Set-AzureRmAnalysisServicesServer
    - Modifica degli SKU hardcoded nella ricerca dinamica.
  * Add-AzureAnalysisServicesAccount per supportare l'accesso con entità servizio
* Automazione
  * Modifiche apportate ai cmdlet AutomationDSC* per eseguire il pull di più di 100 record
  * Risoluzione del problema a causa del quale i flussi dettagliati smettono di funzionare dopo la chiamata di alcuni cmdlet di Automazione, ad esempio Get-AzureRmAutomationVariable e Get-AzureRmAutomationJob.
  * Aggiunta del supporto del controllo delle versioni delle compilazioni di NodeConfiguration in StartAzureAutomationDscCompilationJob e ImportAzureAutomationDscNodeConfiguration
  * Correzioni di bug per problemi esistenti - Correzioni del problema di alias n. 3775 e dell'alias runOn e il supporto per HybridWorkers.
* Calcolo
  * Set-AzureRmVMAEMExtension: aggiunta del supporto per nuove dimensioni dei dischi Premium
  * Set-AzureRmVMAEMExtension: aggiunta del supporto per la serie M
  * Aggiunta del parametro ForceUpdateTag ad Add-AzureRmVmssExtension
  * Aggiunta del parametro Primary a New-AzureRmVmssIpConfig
  * Aggiunta del parametro EnableAcceleratedNetworking ad Add-AzureRmVmssNetworkInterfaceConfig
  * Aggiunta di InstanceId a Set-AzureRmVmss
  * Esposizione di MaintenanceRedeployStatus nell'output -Status di Get-AzureRmVM
  * Esposizione di restrizioni e funzionalità per il formato di tabella di Get-AzureRmComputeResourceSku
* DataLakeStore
  * Correzione per il problema: https://github.com/Azure/azure-powershell/issues/4323
* Hub eventi
  * Aggiunta della proprietà ResourceGroup a NamespaceAttributes
    - 'ResourceGroup' ottiene il nome del gruppo di risorse in cui si trova lo spazio dei nomi
  * Cmdlet aggiornati con set di parametri per spazio dei nomi e hub eventi per il funzionamento della regola di autorizzazione
    - New-AzureRmEventHubAuthorizationRule - Aggiunge una nuova regola di autorizzazione allo spazio dei nomi o all'hub eventi esistente.
    - Get-AzureRmEventHubAuthorizationRule - Ottiene la regola di autorizzazione o un elenco delle regole di autorizzazione per lo spazio dei nomi o l'hub eventi esistente.
    - Set-AzureRmEventHubAuthorizationRule - Aggiorna le proprietà della regola di autorizzazione esistente per l'hub eventi o lo spazio dei nomi.
    - Remove-AzureRmEventHubAuthorizationRule - Elimina la regola di autorizzazione esistente dello spazio dei nomi o dell'hub eventi esistente.
    - New-AzureRmEventHubKey - Genera una nuova chiave primaria/secondaria per la regola di autorizzazione dello spazio dei nomi o dell'hub eventi esistente.
    - Get-AzureRmEventHubKey - Ottiene la chiave primaria/secondaria per la regola di autorizzazione dello spazio dei nomi o dell'hub eventi esistente.
* Rete
    * Aggiunta del supporto per IPv6 e di un nuovo parametro facoltativo - PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: aggiunta del supporto per IPv6. Aggiunta di un nuovo parametro facoltativo
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: aggiunta del supporto per IPv6. Aggiunta di un nuovo parametro facoltativo
    * Parametro contrassegnato come obsoleto - ProbeEnabled
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profilo
    * La raccolta dei dati è abilitata per impostazione predefinita. Microsoft raccoglie dati di utilizzo allo scopo di migliorare l'esperienza utente. I dati sono anonimi e non includono i valori degli argomenti della riga di comando.
      - Usare il cmdlet Disable-AzureRmDataCollection per disattivare la funzionalità
      - Usare il cmdlet Enable-AzureRmDataCollection per attivare questa funzionalità
* Risorse
    * Aggiunta del supporto per la convalida degli ambiti per i cmdlet RoleDefinition e RoleAssignment seguenti prima di inviare la richiesta ad ARM
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * Aggiunta dei nuovi cmdlet seguenti per le regole di autorizzazione per spazio dei nomi, coda e argomento. Le operazioni relative alle regole di autorizzazione vengono eseguite in base al set di parametri.
    - New-AzureRmServiceBusAuthorizationRule - Aggiunge una nuova regola di autorizzazione a spazio dei nomi/coda/argomento del bus di servizio esistente.
    - Get-AzureRmServiceBusAuthorizationRule - Ottiene la regola di autorizzazione/l'elenco delle regole di autorizzazioni per spazio dei nomi/coda/argomento del bus di servizio esistente.
    - Set-AzureRmServiceBusAuthorizationRule - Aggiorna le proprietà della regola di autorizzazione esistente di spazio dei nomi/coda/argomento del bus di servizio.
    - New-AzureRmServiceBusKey - Genera una nuova chiave primaria/secondaria per la regola di autorizzazione di spazio dei nomi/coda/argomento del bus di servizio esistente.
    - Get-AzureRmServiceBusKey - Ottiene la chiave primaria/secondaria per la regola di autorizzazione di spazio dei nomi/coda/argomento del bus di servizio esistente.
    - Remove-AzureRmServiceBusAuthorizationRule - Elimina la regola di autorizzazione esistente di spazio dei nomi/coda/argomento del bus di servizio.
  * Aggiunta della proprietà ResourceGroup a NamespaceAttributes

* Sql
    * Aggiornamento di Set-AzureRmSqlServerTransparentDataEncryptionProtector per visualizzare un avviso e richiedere conferma se il tipo di protezione della crittografia viene impostato su AzureKeyVault
    * Aggiunta di nuovi cmdlet aggiornati per le impostazioni di controllo
      - Cmdlet Get-AzureRmSqlDatabaseAuditing che ottiene le impostazioni di controllo di un database SQL di Azure.
      - Cmdlet Get-AzureRmSqlServerAuditing che ottiene le impostazioni di controllo di un server di Azure SQL.
      - Cmdlet Set-AzureRmSqlDatabaseAuditing che modifica le impostazioni di controllo per un database SQL di Azure.
      - Cmdlet Set-AzureRmSqlServerAuditing che modifica le impostazioni di controllo di un server di Azure SQL.
    * Deprecazione di cmdlet per i criteri di controllo esistenti
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * L'analisi del file di schema per Update-AzureRmSqlSyncGroup ora fa distinzione tra maiuscole e minuscole.
* Archiviazione
    * Aggiunta del supporto di NetworkRule ai cmdlet per l'account di archiviazione in modalità risorsa
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>17.07.2017 - Versione 4.2.1
* Calcolo
  - Correzione del problema relativo ai cmdlet per la creazione e l'aggiornamento di dischi della macchina virtuale e di snapshot di dischi della macchina virtuale, (collegamento)[<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* Profilo
  - Correzione del problema relativo all'autenticazione utente non interattiva in RDFE (collegamento)[<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - Correzione del problema relativo all'autenticazione utente non interattiva (collegamento)[<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>11.7.2017 - Versione 4.2.0
* AnalysisServices
    * Aggiunta di una nuova API per il piano dati
        - Introduzione dell'API per recuperare il log del server di Analysis Services, Export-AzureAnalysisServicesInstanceLog
* Automazione
    * Impostazione corretta del valore TimeZone per le pianificazioni settimanale e mensile per New-AzureRmAutomationSchedule
        - Per altre informazioni, vedere questo problema: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Aggiunta del nuovo cmdlet Get-AzureBatchJobPreparationAndReleaseTaskStatus.
    - Aggiunta di inizio e fine dell'intervallo di byte ai parametri per Get-AzureBatchNodeFileContent.
* CognitiveServices
    * Integrazione con Cognitive Services Management SDK versione 1.0.0.
    * Correzione di un bug relativo al controllo della lunghezza del nome dell'account.
* Calcolo
    * Supporto del tipo di account di archiviazione per il disco immagine:
        - Aggiunta del parametro 'StorageAccountType' a Set-AzureRmImageOsDisk e Add-AzureRmImageDataDisk
    * Funzionalità PrivateIP e PublicIP nella configurazione IP VMSS:
        - Aggiunta dei nomi 'PrivateIPAddressVersion', 'PublicIPAddressConfigurationName', 'PublicIPAddressConfigurationIdleTimeoutInMinutes', 'DnsSetting' a New-AzureRmVmssIpConfig
        - Aggiunta del parametro 'PrivateIPAddressVersion' per specificare IPv4 o IPv6 a New-AzureRmVmssIpConfig
    * Funzionalità di manutenzione delle prestazioni:
        - Aggiunta del parametro opzionale 'PerformMaintenance' a Restart-AzureRmVM.
        - Get-AzureRmVM -Status mostra le informazioni sulla manutenzione delle prestazioni della macchina virtuale specificata
    * Funzionalità di identità della macchina virtuale:
        - Aggiunta del parametro 'IdentityType' a New-AzureRmVMConfig e UpdateAzureRmVM
        - Get-AzureRmVM mostra le informazioni di identità per la macchina virtuale specificata
    * Funzionalità di identità VMSS:
        - Aggiunta del parametro 'IdentityType' a New-AzureRmVmssConfig
        - Get-AzureRmVmss mostra le informazioni di identità per il set di scalabilità di macchine virtuali specificato
    * Funzionalità di diagnostica di avvio VMSS:
        - Nuovo cmdlet per l'impostazione della diagnostica di avvio dell'oggetto VMSS: Set-AzureRmVmssBootDiagnostics
        - Aggiunta del parametro 'BootDiagnostic' a New-AzureRmVmssConfig
    * Funzionalità LicenseType per VMSS:
        - Aggiunta del parametro 'LicenseType' a New-AzureRmVmssConfig
    * Supporto di RecoveryPolicyMode:
        - Aggiunta del parametro 'RecoveryPolicyMode' a New-AzureRmVmssConfig
    * Funzionalità SKU risorse di calcolo:
        - Nuovo cmdlet 'Get-AzureRmComputeResourceSku' per elencare tutte le SKU di risorse di calcolo
* DataFactories
    * Cmdlet New-AzureRmDataFactoryGatewayKey deprecato
    * Introduzione della funzionalità della chiave di autenticazione del gateway con l'aggiunta di New-AzureRmDataFactoryGatewayAuthKey e Get-AzureRmDataFactoryGatewayAuthKey
* DataLakeAnalytics
    * Aggiunta del supporto CRUD per i criteri di calcolo tramite i comandi seguenti:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Aggiunta del supporto dei metadati delle relazioni dei processi per il supporto di processi ricorrenti e pipeline di processi. I comandi seguenti sono stati aggiornati o aggiunti:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * Aggiornamento dei destinatari del token in modo che le API per processi e catalogo possano usare i destinatari specifici di Data Lake corretti, invece dei destinatari risorsa di Azure.
* DataLakeStore
    * Aggiunta del supporto per le rotazioni delle chiavi KeyVault gestite dall'utente nel cmdlet Set-AzureRMDataLakeStoreAccount
    * Aggiunta di un aggiornamento della funzionalità per attivare automaticamente una chiamata `enableKeyVault` quando viene aggiunto un KeyVault gestito dall'utente o si verifica una rotazione di chiave.
    * Aggiornamento dei destinatari del token in modo che le API per processi e catalogo possano usare i destinatari specifici di Data Lake corretti, invece dei destinatari risorsa di Azure.
    * Correzione di un bug limitando le dimensioni dei file creati o aggiunti con i cmdlet seguenti:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* DNS
    * Correzione di un bug nello scenario di pipe per Get-AzureRmDnsZone
        - Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Aggiunta del supporto per abilitare/disabilitare Operations Management Suite (OMS)
    * Nuovi cmdlet
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Aggiunta di nuovi parametri ad Add-AzureRmHDInsightConfigValues per impostare configurazioni personalizzate di Spark
        - Parametri SparkDefaults e SparkThriftConf per Spark 1.6
        - Parametri Spark2Defaults e Spark2ThriftConf per Spark 2.0
* Informazioni dettagliate
    * Problema n. 4215 (richiesta di modifica) rimuovere il limite di 15 giorni nell'intervallo di tempo per il cmdlet Get-AzureRmLog. Inoltre, modifiche di minore entità ai nomi degli unit test.
    * Problema n. 3957 risolto per Get-AzureRmLog
        - Problema n. 1: il back-end restituisce i record in pagine di 200 record ognuna, collegate con il token di continuazione alla pagina successiva. I clienti vedevano restituiti solo 200 record, anche se sapevano che dovevano essercene di più. Il problema si verificava indipendentemente dal valore impostato per MaxEvents, a meno che il valore non fosse minore di 200.
        - Problema n. 2: la documentazione conteneva dati errati su questo cmdlet, ad esempio il valore predefinito per l'intervallo di tempo era di 1 ora.
        - Correzione n. 1: il cmdlet segue ora il token di continuazione restituito dal back-end fino a raggiungere MaxEvents o la fine del set.<br>Il valore predefinito per MaxEvents è 1000 e il valore massimo è 100000. Qualsiasi valore per MaxEvents minore di 1 viene ignorato e viene invece usato il valore predefinito. Questi valori e il comportamento non sono cambiati, ma ora sono documentati in modo corretto.<br>È stato aggiunto l'alias MaxRecords per MaxEvents, dato che il nome del cmdlet non indica più gli eventi, ma solo i log.
        - Correzione n. 2: la documentazione contiene informazioni corrette e più dettagliate: nuovo alias, intervallo di tempo corretto, impostazione predefinita corretta, valori minimo e massimo.
* Insieme di credenziali delle chiavi
    * Rimozione dell'indirizzo di posta elettronica dalla query sulla directory quando si specifica -UserPrincipalName per i cmdlet Set-AzureRMKeyVaultAccessPolicy e Remove-AzureRMKeyVaultAccessPolicy.
      - Entrambi i cmdlet includono ora il parametro -EmailAddress che può essere usato al posto del parametro -UserPrincipalName quando è appropriato eseguire query per ottenere l'indirizzo di posta elettronica.  Se sono presenti più indirizzi di posta elettronica corrispondenti nella directory, l'esecuzione del cmdlet avrà esito negativo.
* Rete
    * New-AzureRmIpsecPolicy: i parametri SALifeTimeSeconds e SADataSizeKilobytes non sono più obbligatori
        - Il valore predefinito per SALifeTimeSeconds è 27000 secondi
        - Il valore predefinito per SADataSizeKilobytes è 102400000 KB
    * Aggiunto il supporto per la configurazione di un pacchetto di crittografia personalizzato con criteri SSL e per elencare tutte le API per opzioni SSL nel gateway applicazione
        - Aggiunta dei parametri facoltativi -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Aggiunta di Get-AzureRmApplicationGatewayAvailableSslOptions (Alias: List-AzureRmApplicationGatewayAvailableSslOptions)
        - Aggiunta di Get-AzureRmApplicationGatewaySslPredefinedPolicy (Alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Aggiunta del supporto del reindirizzamento nel gateway applicazione
        - Aggiunta di Add-AzureRmApplicationGatewayRedirectConfiguration
        - Aggiunta di Get-AzureRmApplicationGatewayRedirectConfiguration
        - Aggiunta di New-AzureRmApplicationGatewayRedirectConfiguration
        - Aggiunta di Remove-AzureRmApplicationGatewayRedirectConfiguration
        - Aggiunta di Set-AzureRmApplicationGatewayRedirectConfiguration
        - Aggiunta del parametro facoltativo - RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Aggiunta del parametro facoltativo - DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Aggiunta del parametro facoltativo - RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Aggiunta del parametro facoltativo - RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Aggiunta del supporto per i siti Web di Azure nel gateway applicazione
        - Aggiunta di New-AzureRmApplicationGatewayProbeHealthResponseMatch
        - Aggiunta dei parametri facoltativi -PickHostNameFromBackendHttpSettings, -MinServers, -Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Aggiunta dei parametri facoltativi -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Aggiunta di Get-AzureRmPublicIPaddress per recuperare le risorse di tipo indirizzo IP pubblico create tramite un set di scalabilità di macchine virtuali
    * Aggiunta di un cmdlet per ottenere l'utilizzo corrente della rete virtuale
        - Get-AzureRmVirtualNetworkUsageList
* Profilo
    * Correzione dell'errore che si verifica durante l'uso di Import-AzureRmContext o Save-AzureRmContext
        - Per altre informazioni, vedere questo problema: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Introduzione di un nuovo modulo per le operazioni su Azure Site Recovery.
        - Tutti i cmdlet iniziano con AzureRmRecoveryServicesAsr*
* Sql
    * Aggiunta dei cmdlet di PowerShell per la sincronizzazione dati in AzureRM.Sql
    * Aggiornamento dei cmdlet AzureRmSqlServer per l'uso della nuova versione dell'API REST che evita timeout durante la creazione del server.
    * I cmdlet di aggiornamento del server sono deprecati perché la versione precedente del server (2.0) non esiste più.
    * Aggiunta del nuovo parametro facoltativo "AssignIdentity" ai cmdlet New-AzureRmSqlServer e Set-AzureRmSqlServer per supportare il provisioning di un'identità per la risorsa SQL Server
    * Il parametro ResourceGroupName è ora facoltativo per Get-AzureRmSqlServer
        - Per altre informazioni, vedere il problema seguente: https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement per ExpressRoute:
    * Aggiornamento del cmdlet New-AzureBgpPeering per aggiungere le nuove opzioni seguenti:
        - PeerAddressType: è possibile specificare i valori "IPv4" o "IPv6" per creare un peering BGP con il tipo di famiglia di indirizzi corrispondente
    * Aggiornamento del cmdlet Set-AzureBgpPeering per aggiungere le nuove opzioni seguenti:
        - PeerAddressType: è possibile specificare i valori "IPv4" o "IPv6" per aggiornare un peering BGP con il tipo di famiglia di indirizzi corrispondente
    * Aggiornamento del cmdlet Remove-AzureBgpPeering per aggiungere le nuove opzioni seguenti:
        - PeerAddressType: è possibile specificare i valori "IPv4", "IPv6"o "All" per rimuovere un peering BGP con il tipo di famiglia di indirizzi corrispondente oppure per rimuoverli tutti

## <a name="20170607---version-410"></a>07.06.2017 - Versione 4.1.0
* AnalysisServices
    * Nuove SKU aggiunte: B1, B2, S0
    * Aggiunto il supporto per la scalabilità orizzontale/verticale
* CognitiveServices
    * Aggiornamento della visualizzazione dettagliata dei contratti di licenza durante la creazione di risorse di Servizi cognitivi
* Calcolo
    * Correzione di Fix Test-AzureRmVMAEMExtension per le macchine virtuali con più dischi gestiti
    * Aggiornamento di Set-AzureRmVMAEMExtension: aggiunta delle informazioni per la memorizzazione nella cache per i dischi gestiti Premium
    * Add-AzureRmVhd: aumento del limite di dimensioni per il disco rigido virtuale a 4 TB.
    * Stop-AzureRmVM: chiarimenti nella documentazione per il parametro STayProvisioned
    * New-AzureRmDiskUpdateConfig
      * Parametri CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId deprecati
    * Set-AzureRmDiskUpdateImageReference: cmdlet deprecato
    * New-AzureRmSnapshotUpdateConfig
      * Parametri CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId deprecati
    * Set-AzureRmSnapshotUpdateImageReference: cmdlet deprecato
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Abilitazione della crittografia gestita KeyVault per un archivio Data Lake
* DevTestLabs
    * Aggiornamento dei cmdlet per il supporto della versione dell'API DevTest Labs corrente e aggiornata.
* IotHub
    * Aggiunta del supporto di routing per i cmdlet IoTHub
* Insieme di credenziali delle chiavi
  * Nuovi cmdlet per il supporto di chiavi dell'account di archiviazione gestite da KeyVault
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Rete
    * Get-AzureRmNetworkUsage: nuovo cmdlet per visualizzare dettagli sull'utilizzo e la capacità della rete
    * Aggiunta di nuove opzioni GatewaySku per VirtualNetworkGateways
        * VpnGw1, VpnGw2, VpnGw3 sono le nuove SKU aggiunte per i gateway VPN
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Correzione di esempi della Guida
* NotificationHubs
    * Aggiornamento trasparente dei cmdlet NotificationHubs per la nuova API
* Profilo
    * Resolve-AzureRmError
      * Nuovo cmdlet per visualizzare i dettagli degli errori e delle eccezioni generati dai cmdlet, inclusi dati relativi a richieste/risposte del server
    * Send-Feedback
      * Abilitazione dell'invio di commenti e suggerimenti senza effettuare l'accesso
    * Get-AzureRmSubscription
      * Correzione di un bug relativo al recupero di sottoscrizioni CSP
* Risorse
    * Risoluzione di un problema a causa del quale Get-AzureRMRoleAssignment genera un errore di richiesta non valida se il numero di assegnazioni di ruolo è maggiore di 1000
        * Gli utenti possono ora usare Get-AzureRMRoleAssignment, anche se le assegnazioni di ruolo da restituire sono più di 1000
* Sql
    * Restore-AzureRmSqlDatabase: aggiornamento di un esempio nella documentazione
* Archiviazione
    * Aggiunta del supporto dell'impostazione AssignIdentity ai cmdlet per l'account di archiviazione in modalità risorsa
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Aggiunta del supporto della chiave del cliente ai cmdlet per l'account di archiviazione in modalità risorsa
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Nuove impostazioni di monitoraggio 'MonitorIntervalInSeconds', 'MonitorTimeoutInSeconds', 'MonitorToleratedNumberOfFailures'
    * Nuovo protocollo per il monitoraggio 'TCP'
* ServiceManagement
    * Add-AzureVhd: aumento del limite di dimensioni per il disco rigido virtuale a 4 TB.
    * New-AzureBGPPeering: supporto di LegacyMode
* Azure.Storage
    * Aggiornamento della Guida per i parametri che accettano caratteri jolly e aggiornamento del tipo StorageContext

## <a name="20170523---version-402"></a>23.05.2017 - Versione 4.0.2
* Profilo
    * Add-AzureRmAccount
      * Aggiunta dell'alias del parametro `-EnvironmentName` per compatibilità con le versioni 2.x di AzureRM.profile

## <a name="20170512---version-401"></a>12.05.2017 - Versione 4.0.1
 * Correzione del problema relativo a New-AzureStorageContext in scenari offline: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>10.05.2017 - Versione 4.0.0


* Questa versione contiene modifiche di rilievo. Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per dettagli sulle modifiche e sull'impatto sugli script esistenti.
* Gestione API
  - Aggiunta del supporto per la configurazione di gruppi esterni in New-AzureRmApiManagementGroup.
* Fatturazione
  - Nuovo cmdlet Get-AzureRmBillingPeriod
    + cmdlet per recuperare i periodi di fatturazione Azure della sottoscrizione.
  - Aggiornamento del cmdlet Get-AzureRmBillingInvoice
  - nuova proprietà BillingPeriodNames
  - output nella visualizzazione elenco
* Calcolo
  - Aggiornamento dei cmdlet Set-AzureRmVMAEMExtension e Test-AzureRmVMAEMExtension per il supporto di Managed Disks Premium
  - Backup delle impostazioni di crittografia per le macchine virtuali IaaS e ripristino in caso di errore
  - L'opzione ChefServiceInterval è stata rinominata ChefDaemonInterval. Quella precedente continuerà comunque a funzionare.
  - Rimozione delle proprietà DataDiskNames e NetworkInterfaceIDs duplicate dall'oggetto PS VM.
  - Rendere i parametri DataDiskNames e NetworkInterfaceIDs facoltativi, rispettivamente in Remove-AzureRmVMDataDisk e Remove-AzureRmVMNetworkInterface.
  - Correzione del problema dei pipe dei cmdlet Get nel caso in cui restituiscano un oggetto elenco.
  - Ridenominazione dei cmdlet che erano in conflitto con i cmdlet RDFE. Per maggiori dettagli, vedere il problema https://github.com/Azure/azure-powershell/issues/2917
    + `New-AzureVMSqlServerAutoBackupConfig` è stata rinominata `New-AzureRmVMSqlServerAutoBackupConfig`
    + `New-AzureVMSqlServerAutoPatchingConfig` è stata rinominata `New-AzureRmVMSqlServerAutoPatchingConfig`
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` è stata rinominata `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* Consumo
  - Nuovo cmdlet Get-AzureRmConsumptionUsageDetail
    + cmdlet per recuperare i dettagli d'uso della sottoscrizione.
* ContainerRegistry
  - Aggiunta di cmdlet PowerShell per il Registro contenitori di Azure
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Aggiunta del supporto per l'acquisizione e la presentazione del pacchetto catalogo
  - Aggiunta del supporto per la presentazione dei seguenti elementi del catalogo dai predecessori più approfonditi:
    + Tabella
    + Funzione con valori di tabella
    + Visualizza
    + Statistiche
* DataLakeStore
  - Per impostazione predefinita, la registrazione traccia per `Import-AzureRMDataLakeStoreItem` e `Export-AzureRMDataLakeStoreItem` è stata disabilitata per migliorare le prestazioni. Se si desidera la registrazione traccia, usare i parametri `-DiagnosticLogLevel` e `-DiagnosticLogPath`
  - Correzione di un bug che causava talvolta l'arresto anomalo di PowerShell durante il caricamento di molti file di piccole dimensioni in ADLS.
* Hub eventi
  - Correzione di bug:
    + Correzione dell'errore 'Tier' cannot be null, where it should be 'SkuName' ("Tier" non può essere Null quando dovrebbe essere "Skuname") per il cmdlet Set-AzureRmEventHubNamespace
    + Set-AzureRmEventHub - Correzione dell'errore "Riferimento a un oggetto non impostato su un'istanza di oggetto." durante l'aggiornamento di EventHub
* Informazioni dettagliate
  - Add-AzureRm*AlertRule
    + Restituisce un singolo oggetto: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + L'output è ora enumerato anziché essere considerato un singolo oggetto. Il tipo non è stato modificato ed è sempre un elenco.
  - Remove-AzureRmAlertRule
    + statusCode segue il codice di stato restituito dalla richiesta mentre prima era sempre Ok.
  - Add-AzureRmAutoscaleSetting
    + Ora restituisce un oggetto singolo (e non un elenco come prima) contenente statusCode, requestId e la risorsa appena creata/aggiornata.
    + Il codice di stato segue lo stato restituito dalla richiesta mentre prima era sempre Ok.
  - New-AzureRmAutoscaleRule
    + Il parametro ScaleActionType è stato esteso ed accetta ora i seguenti valori: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + statusCode nell'output segue lo statusCode restituito dalla richiesta. Prima, era sempre Ok.
  - Get-AzureRMLogProfile
    + L'output è ora enumerato. Prima era considerato un singolo oggetto. Il tipo di output continua a essere un elenco, come prima.
  - Remove-AzureRmLogProfile
    + Il parametro PassThru è stato implementato.
  - Metriche API
    + SDK recupera ora le metriche da MDM.
  - Get-AzureRmMetricDefinition
    + L'output è ancora un elenco, ma la struttura dell'elenco è stata modificata.
  - Get-AzureRmMetric
    + La chiamata è stata modificata. Questa è la nuova sintassi: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + L'output è un elenco e la struttura dei suoi elementi è stata modificata.
* Insieme di credenziali delle chiavi
  - Aggiunta del supporto per il backup/ripristino dei segreti KeyVault
    + È possibile eseguire il backup e il ripristino dei segreti come con la funzionalità attualmente supportata per Chiavi

  - I cmdlet di backup per Chiavi e Segreti accettano ora un oggetto corrispondente come parametro di input
    + Il chiamante può concatenare le operazioni di recupero e backup: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - I cmdlet di backup supportano ora un'opzione -Force per la sovrascrittura di un file esistente
    + Si noti che il tentativo di sovrascrivere un file esistente non genera più un'istruzione Throw ma richiede invece all'utente di scegliere come procedere.
* LogicApp
  - Nuovi parametri per i cmdlet di ripristino di emergenza del numero di controllo interscambio:
    + Parametro -AgreementType facoltativo ("X12" o "Edifact") per specificare i numeri di controllo pertinenti
* MachineLearning
  - Uso della nuova versione di Azure Machine Learning .Net SDK ed aggiunta di un nuovo cmdlet
    + Add-AzureRmMlWebServiceRegionalProperty
  - Lievi correzioni al testo della Guida.
* Rete
  - Aggiunta del cmdlet Test-AzureRmNetworkWatcherConnectivity
    + Restituisce informazioni sulla connessione per una macchina virtuale di origine specificata e una destinazione
    + Se non è possibile stabilire una connessione tra l'origine e la destinazione, il cmdlet restituisce dettagli sul problema
* Profilo
  - Aggiunta del cmdlet `Send-Feedback': consente all'utente di iniziare un set di prompt che inviano commenti al team di Azure PowerShell.
  - Sono stati rimossi i seguenti alias perché erano in conflitto con i nomi dei cmdlet esistenti nel modulo Azure:
    + `Enable-AzureDataCollection` (supportato da `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (supportato da `Disable-AzureRmDataCollection`)
* Relay
  - Aggiunge cmdlet per Inoltro di Azure che consente agli utenti di creare e gestire tutte le risorse di Inoltro di Azure.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Risorse
  - Supporto per le distribuzioni cross-resource-group per New-AzureRmResourceGroupDeployment
    + Gli utenti possono ora usare le distribuzioni nidificate per distribuire gruppi di risorse diversi.
* ServiceBus

  - Correzione di bug: i valori della proprietà oggetto ServiceBus Queue erano impostati su Null. L'oggetto è usato come parametro di input nel cmdlet Set-AzureRmServiceBusQueue cmdlet per aggiornare Queue.
    - Le proprietà interessate sono LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount e MessageCount
* ServiceFabric

  - Aggiunta di cmdlet per Service Fabric
    + Add-AzureRmServiceFabricApplicationCertificate       Aggiunge un certificato che verrà usato come certificato applicazione
    + Add-AzureRmServiceFabricClientCertificate       Aggiunge un nome comune o un'identificazione personale alle impostazioni cluster per l'autenticazione client
    + Add-AzureRmServiceFabricClusterCertificate       Aggiunge un certificato cluster secondario al cluster per la sostituzione del certificato esistente
    + Add-AzureRmServiceFabricNodes       Aggiunge nodi/macchine virtuali di un tipo di nodo specifico a un cluster
    + Add-AzureRmServiceFabricNodeType       Aggiunge un tipo di nodo/macchina virtuale a un cluster esistente
    + Get-AzureRmServiceFabricCluster       Ottiene i dettagli della risorsa cluster
    + New-AzureRmServiceFabricCluster Crea un nuovo cluster ServiceFabric. Questo comando ha molti overload per coprire vari scenari
    + Remove-AzureRmServiceFabricClientCertificate       Rimuove un certificato client perché non venga usato per accedere a un cluster
    + Remove-AzureRmServiceFabricClusterCertificate       Rimuove un certificato cluster perché non possa essere usato per la protezione del cluster
    + Remove-AzureRmServiceFabricNodes       Rimuove i nodi di un tipo di nodo specifico da un cluster
    + Remove-AzureRmServiceFabricNodeType       Rimuove un tipo di nodo da un cluster
    + Remove-AzureRmServiceFabricSettings       Rimuove una o più impostazioni ServiceFabric da un cluster
    + Set-AzureRmServiceFabricSettings       Aggiunge o aggiorna una o più impostazioni ServiceFabric di un cluster
    + Set-AzureRmServiceFabricUpgradeType       Modifica il tipo di aggiornamento ServiceFabric di un cluster
    + Update-AzureRmServiceFabricDurability       Modifica il livello di durabilità di un cluster
    + Update-AzureRmServiceFabricReliability       Modifica il livello di affidabilità di un cluster
* Sql
  - Aggiunta del parametro -SampleName a New-AzureRmSqlDatabase
  - Aggiornamenti ai cmdlet di Gruppo di failover
  - Rimozione dei parametri "Tag"
  - Rimozione dei parametri "PartnerResourceGroupName" e "PartnerServerName" dal cmdlet Remove-AzureRmSqlDatabaseFailoverGroup
  - Aggiunta del parametro "GracePeriodWithDataLossHours" ai cmdlet New- e Set-, che sostituiranno comunque "GracePeriodWithDataLossHour"
  - Approfondimento e aggiornamento della documentazione
  - Modifica della formattazione degli oggetti restituiti e correzione di alcuni bug quando i campi non erano sempre popolati
  - Aggiunta delle proprietà "DatabaseNames" e "PartnerLocation" all'oggetto Gruppo di failover
  - Correzione di un bug che causava la restituzione immediata del cmdlet Switch- anziché al termine dell'operazione
  - Correzione del bug di overflow di numero intero per l'uso di valori alti per il periodo di tolleranza
  - Rettifica del periodo di tolleranza su un minimo di 1 ora se quello specificato è minore
  - Rimozione di "Usage_Anomaly" dai valori accettati per il parametro "ExcludedDetectionType" dei cmdlet Set-AzureRmSqlDatabaseThreatDetectionPolicy e Set-AzureRmSqlServerThreatDetectionPolicy.
* Archiviazione
  - Aggiornamento di SRP SDK alla versione 6.3.0
  - New/Set-AzureRmStorageAccount: aggiunta di un nuovo parametro per supportare EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount: l'account di archiviazione restituito contiene un nuovo attributo EnableHttpsTrafficOnly
* Azure.Storage
  - Aggiornamento ad Azure Storage Client Library 8.1.1 e Azure Storage DataMovement Library 0.5.1
  - Aggiunta di un nuovo cmdlet per supportare la funzionalità blob Incremental Copy (Copia incrementale)
