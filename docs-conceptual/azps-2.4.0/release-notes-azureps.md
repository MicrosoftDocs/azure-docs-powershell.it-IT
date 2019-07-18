---
ms.openlocfilehash: f357a17f698d68c1a29dcb78f83671973fd6ecad
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863731"
---
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
    - [Altre](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR
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
* Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
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
* Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
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
* Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
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