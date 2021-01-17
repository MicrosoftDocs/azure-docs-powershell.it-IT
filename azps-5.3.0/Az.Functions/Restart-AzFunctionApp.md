---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476282"
---
# Restart-AzFunctionApp

## Sinossi
Riavvia un'app di funzione.

## SINTASSI

### RestartByName (impostazione predefinita)
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## Descrizione
Riavvia un'app di funzione.

## ESEMPI

### Esempio 1: ottenere un'app di funzione per nome e riavviarla.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

Questo comando consente di ottenere un'app di funzione per nome e di riavviarla.

### Esempio 2: riavviare un'app di funzione per nome.
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Questo comando riavvia un'app di funzione per nome.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Impone al cmdlet di riavviare l'app della funzione senza richiedere conferma.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome dell'app funzione.

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce vero quando il comando riesce.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID abbonamento di Azure.

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite

## OUTPUT

### System. Boolean

## Note

ALIAS

PROPRIETÀ COMPLESSE DI PARAMETRI

Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Percorso delle risorse.
  - `CloningInfoSourceWebAppId <String>`: ID risorsa ARM dell'app di origine. ID risorsa dell'app è il formato/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} per gli slot di produzione e/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} per altri slot.
  - `[Kind <String>]`: Tipo di risorsa.
  - `[Tag <IResourceTags>]`: Tag delle risorse.
    - `[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> per abilitare l'affinità del client <code>false</code> , per interrompere l'invio di cookie di affinità della sessione, che instradano le richieste client nella stessa sessione alla stessa istanza. Il valore predefinito è <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> per abilitare l'autenticazione del certificato client (TLS Mutual Authentication); in caso contrario, <code>false</code> . Il valore predefinito è <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: percorsi di esclusione separati da virgola con autenticazione del certificato client
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: L'impostazione dell'applicazione sostituisce l'app clonata. Se specificato, queste impostazioni sostituiscono le impostazioni clonate dall'app di origine. In caso contrario, vengono mantenute le impostazioni delle applicazioni dall'app di origine.
    - `[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> per clonare hostname personalizzati dall'app di origine; in caso contrario, <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> per clonare il controllo del codice sorgente dall'app di origine; in caso contrario <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> per configurare il bilanciamento del carico per l'app di origine e destinazione.
  - `[CloningInfoCorrelationId <String>]`: ID correlazione dell'operazione di clonazione. Questo ID unisce più operazioni di clonazione insieme per usare lo stesso snapshot.
  - `[CloningInfoHostingEnvironment <String>]`: Ambiente di servizio app.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> per sovrascrivere l'app di destinazione; in caso contrario, <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Posizione di origine app ex: ovest degli Stati Uniti o Nord Europa
  - `[CloningInfoTrafficManagerProfileId <String>]`: ID risorsa ARM del profilo di gestione traffico da usare, se esistente. ID risorsa del gestore del traffico con il formato/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Nome del profilo di Traffic Manager da creare. Questa operazione è necessaria solo se il profilo di Traffic Manager non esiste già.
  - `[Config <ISiteConfig>]`: Configurazione dell'app.
    - `IsPushEnabled <Boolean>`: Ottiene o imposta un contrassegno che indica se l'endpoint push è abilitato.
    - `[ActionMinProcessExecutionTime <String>]`: Tempo minimo necessario per l'esecuzione del processo prima di eseguire l'azione
    - `[ActionType <AutoHealActionType?>]`: Azione predefinita da intraprendere.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> se è sempre attivato; in caso contrario, <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: URL della definizione dell'API.
    - `[ApiManagementConfigId <String>]`: APIM-Api identificatore.
    - `[AppCommandLine <String>]`: Riga di comando dell'app da avviare.
    - `[AppSetting <INameValuePair[]>]`: Impostazioni applicazione.
      - `[Name <String>]`: Nome coppia.
      - `[Value <String>]`: Valore pair.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> se l'opzione Correzione automatica è abilitata; in caso contrario, <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Nome dello slot di scambio automatico.
    - `[ConnectionString <IConnStringInfo[]>]`: Stringhe di connessione.
      - `[ConnectionString <String>]`: Valore stringa di connessione.
      - `[Name <String>]`: Nome della stringa di connessione.
      - `[Type <ConnectionStringType?>]`: Tipo di database.
    - `[CorAllowedOrigin <String[]>]`: Ottiene o imposta l'elenco di origini che devono essere consentite per effettuare chiamate tra origini, ad esempio: http://example.com:12345) . Usare "*" per consentire tutti.
    - `[CorSupportCredentials <Boolean?>]`: Ottiene o imposta se sono consentite le richieste di CORS con le credenziali. https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsPer altre informazioni, vedere.
    - `[CustomActionExe <String>]`: Eseguibile da eseguire.
    - `[CustomActionParameter <String>]`: Parametri per l'eseguibile.
    - `[DefaultDocument <String[]>]`: Documenti predefiniti.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione dettagliata degli errori; in caso contrario, <code>false</code> .
    - `[DocumentRoot <String>]`: Radice del documento.
    - `[DynamicTagsJson <String>]`: Ottiene o imposta una stringa JSON contenente un elenco di tag dinamici che verranno valutati dalle attestazioni degli utenti nell'endpoint di registrazione push.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Elenco delle regole di rampa.
      - `[ActionHostName <String>]`: Hostname di uno slot a cui verrà reindirizzato il traffico, se deciso. Ad esempio. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: L'algoritmo decisionale personalizzato può essere fornito nell'estensione del sito di TiPCallback, quale URL può essere specificato. Vedere estensione del sito TiPCallback per il patibolo e i contratti.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Specifica l'intervallo in minuti per rivalutare ReroutePercentage.
      - `[ChangeStep <Double?>]`: Nello scenario rampa automatica questo è il passaggio da cui aggiungere/rimuovere <code>ReroutePercentage</code> fino a quando non raggiunge \n <code>MinReroutePercentage</code> o         <code>MaxReroutePercentage</code> . Le metriche del sito vengono controllate ogni N minuti specificato nell' <code>ChangeIntervalInMinutes</code> algoritmo di decisione .\nCustom può essere fornito nell'estensione del sito TiPCallback in cui è possibile specificare l'URL <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Specifica il limite superiore al di sotto del quale ReroutePercentage rimarrà.
      - `[MinReroutePercentage <Double?>]`: Specifica il contorno inferiore sopra il quale ReroutePercentage rimarrà.
      - `[Name <String>]`: Nome della regola di routing. Il nome consigliato consiste nel puntare allo slot che riceverà il traffico nell'esperimento.
      - `[ReroutePercentage <Double?>]`: Percentuale del traffico a cui verrà reindirizzato <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: Stato del servizio FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Mapping dei gestori.
      - `[Argument <String>]`: Argomenti della riga di comando da passare al processore di script.
      - `[Extension <String>]`: Le richieste con questa estensione verranno gestite con l'applicazione specificata FastCGI.
      - `[ScriptProcessor <String>]`: Il percorso assoluto dell'applicazione FastCGI.
    - `[HealthCheckPath <String>]`: Percorso di controllo integrità
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: configura un sito Web per consentire ai client di connettersi tramite http 2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se la registrazione http è abilitata; in caso contrario, <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrizioni di sicurezza IP per Main.
      - `[Action <String>]`: Consenti o negare l'accesso per questo intervallo IP.
      - `[Description <String>]`: Descrizione della regola di restrizione IP.
      - `[IPAddress <String>]`: Indirizzo IP per cui è valida la restrizione di sicurezza.         Può essere in forma di indirizzo IPv4 puro (proprietà submask necessaria) o notazione CIDR, ad esempio IPv4/Mask (corrispondenza di bit iniziale). Per la notazione CIDR, la proprietà submask non deve essere specificata.
      - `[Name <String>]`: Nome regola di restrizione IP.
      - `[Priority <Int32?>]`: Priorità della regola di restrizione IP.
      - `[SubnetMask <String>]`: Subnet mask per l'intervallo di indirizzi IP per cui è valida la restrizione.
      - `[SubnetTrafficTag <Int32?>]`: tag di traffico subnet (interno)
      - `[Tag <IPFilterTag?>]`: Definisce l'uso di questo filtro IP. Questo per supportare il filtro IP sui proxy.
      - `[VnetSubnetResourceId <String>]`: ID risorsa di rete virtuale
      - `[VnetTrafficTag <Int32?>]`: (interno) VNET traffico
    - `[JavaContainer <String>]`: Contenitore Java.
    - `[JavaContainerVersion <String>]`: Versione contenitore Java.
    - `[JavaVersion <String>]`: Versione Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Utilizzo massimo consentito per le dimensioni del disco in MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Utilizzo massimo consentito della memoria in MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Percentuale massima di utilizzo della CPU consentita.
    - `[LinuxFxVersion <String>]`: Framework e versione dell'app Linux
    - `[LoadBalancing <SiteLoadBalancing?>]`: Bilanciamento del carico del sito.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> per abilitare MySQL locale; in caso contrario, <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: Limite di dimensione della directory registri HTTP.
    - `[MachineKeyDecryption <String>]`: Algoritmo usato per la decrittografia.
    - `[MachineKeyDecryptionKey <String>]`: Chiave di decrittografia.
    - `[MachineKeyValidation <String>]`: Convalida MachineKey.
    - `[MachineKeyValidationKey <String>]`: Chiave di convalida.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Modalità pipeline gestita.
    - `[ManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura la versione minima di TLS necessaria per le richieste SSL
    - `[NetFrameworkVersion <String>]`: Versione di .NET Framework.
    - `[NodeVersion <String>]`: Versione di Node.js.
    - `[NumberOfWorker <Int32?>]`: Numero di lavoratori.
    - `[PhpVersion <String>]`: Versione di PHP.
    - `[PowerShellVersion <String>]`: Versione di PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Numero di istanze preriscaldate.         Questa impostazione si applica solo ai piani consumi e elastici
    - `[PublishingUsername <String>]`: Nome utente di pubblicazione.
    - `[PushKind <String>]`: Tipo di risorsa.
    - `[PythonVersion <String>]`: Versione di Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se il debug remoto è abilitato; in caso contrario, <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Versione di debug remoto.
    - `[RequestCount <Int32?>]`: Richiedi conteggio.
    - `[RequestTimeInterval <String>]`: Intervallo di tempo.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> se l'analisi delle richieste è abilitata; in caso contrario, <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Richiedi ora di scadenza dell'analisi.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrizioni di sicurezza IP per SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrizioni di sicurezza IP per SCM per l'uso di Main.
    - `[ScmType <ScmType?>]`: Tipo SCM.
    - `[SlowRequestCount <Int32?>]`: Richiedi conteggio.
    - `[SlowRequestTimeInterval <String>]`: Intervallo di tempo.
    - `[SlowRequestTimeTaken <String>]`: Tempo impiegato.
    - `[TagWhitelistJson <String>]`: Ottiene o imposta una stringa JSON contenente un elenco di tag whitelist per l'uso da parte dell'endpoint di registrazione push.
    - `[TagsRequiringAuth <String>]`: Ottiene o imposta una stringa JSON contenente un elenco di tag che richiedono l'utilizzo dell'autenticazione utente nell'endpoint di registrazione push.         I tag possono essere costituiti da caratteri alfanumerici e i seguenti:' _',' @',' #',' .',':','-'.         La convalida deve essere eseguita in PushRequestHandler.
    - `[TracingOption <String>]`: Opzioni di traccia.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Regola basata sui byte privati.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Regola basata sui codici di stato.
      - `[Count <Int32?>]`: Richiedi conteggio.
      - `[Status <Int32?>]`: Codice di stato HTTP.
      - `[SubStatus <Int32?>]`: Richiedi stato secondario.
      - `[TimeInterval <String>]`: Intervallo di tempo.
      - `[Win32Status <Int32?>]`: Codice di errore Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> per usare il processo di lavoro a 32 bit; in caso contrario, <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Applicazioni virtuali.
      - `[PhysicalPath <String>]`: Percorso fisico.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> se il precaricamento è abilitato; in caso contrario, <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Directory virtuali per l'applicazione virtuale.
        - `[PhysicalPath <String>]`: Percorso fisico.
        - `[VirtualPath <String>]`: Percorso dell'applicazione virtuale.
      - `[VirtualPath <String>]`: Percorso virtuale.
    - `[VnetName <String>]`: Nome rete virtuale.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket è abilitato; in caso contrario, <code>false</code> .
    - `[WindowsFxVersion <String>]`: Framework e versione per le app Xenon
    - `[XManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito esplicito
  - `[ContainerSize <Int32?>]`: Dimensioni del contenitore di funzioni.
  - `[DailyMemoryTimeQuota <Int32?>]`: Quota massima di memoria giornaliera consentita (applicabile solo per le app dinamiche).
  - `[Enabled <Boolean?>]`: <code>true</code> se l'app è abilitata; in caso contrario, <code>false</code> . L'impostazione di questo valore su false disabilita l'app (l'app non è in linea).
  - `[HostNameSslState <IHostNameSslState[]>]`: Gli Stati SSL del nome host vengono usati per gestire i binding SSL per i nomi host dell'app.
    - `[HostType <HostType?>]`: Indica se il nome host è un nome host standard o repository.
    - `[Name <String>]`Hostname.
    - `[SslState <SslState?>]`: Tipo SSL.
    - `[Thumbprint <String>]`: Identificazione personale del certificato SSL.
    - `[ToUpdate <Boolean?>]`: Impostato su <code>true</code> per aggiornare il nome host esistente.
    - `[VirtualIP <String>]`: Indirizzo IP virtuale assegnato al nome host se è abilitato il protocollo SSL basato su IP.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> per disabilitare i nomi host pubblici dell'app; in caso contrario, <code>false</code> .          Se <code>true</code> l'app è accessibile solo tramite il processo di gestione delle API.
  - `[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente di servizio app.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: configura un sito Web in cui accettare solo le richieste HTTPS. Problemi di reindirizzamento per le richieste http
  - `[HyperV <Boolean?>]`: Sandbox Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Tipo di identità del servizio gestito.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: L'elenco delle identità assegnate dall'utente associato alla risorsa. I riferimenti chiave del dizionario delle identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[IsXenon <Boolean?>]`: Obsolete: sandbox Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: Modalità di ridondanza del sito
  - `[Reserved <Boolean?>]`: <code>true</code> se riservato; in caso contrario, <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> per arrestare il sito SCM (kudu) quando l'app viene arrestata; in caso contrario, <code>false</code> . Il valore predefinito è <code>false</code> .
  - `[ServerFarmId <String>]`: ID risorsa del piano di servizio app associato, formattato come: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## COLLEGAMENTI CORRELATI

