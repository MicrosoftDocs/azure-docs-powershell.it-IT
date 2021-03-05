---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionApp.md
ms.openlocfilehash: 8747cd4bbe6c6b53474597157a0676ec9fef110a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994249"
---
# Remove-AzFunctionApp

## SYNOPSIS
Elimina un'app per le funzioni.

## SINTASSI

### ByName (Impostazione predefinita)
```
Remove-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Elimina un'app per le funzioni.

## ESEMPI

### Esempio 1: Ottenere un'app per le funzioni in base al nome ed eliminarla.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionApp -Force
```

Questo comando recupera un'app per funzione in base al nome ed elimina l'app.

### Esempio 2: Eliminare un'app per funzioni in base al nome.
```powershell
PS C:\> Remove-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Questo comando elimina un'app per funzioni in base al nome.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Forza il cmdlet a rimuovere l'app funzione senza chiedere conferma.

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
Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.

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

### -Name
Nome dell'app per le funzioni.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce true quando il comando ha esito positivo.

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
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID sottoscrizione di Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## OUTPUT

### System.Boolean

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Posizione risorsa.
  - `CloningInfoSourceWebAppId <String>`: ARM ID risorsa dell'app di origine. L'ID risorsa app ha il formato /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} per gli slot di produzione e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} per altri slot.
  - `[Kind <String>]`: tipo di risorsa.
  - `[Tag <IResourceTags>]`: tag di risorsa.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[ClientAffinityEnabled <Boolean?>]`: per abilitare l'affinità client, interrompere l'invio di cookie di affinità di sessione, che instradino le richieste client nella stessa sessione <code>true</code> <code>false</code> alla stessa istanza. L'impostazione predefinita è <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> per abilitare l'autenticazione del certificato client (autenticazione a comune TLS); in caso contrario, <code>false</code> . L'impostazione predefinita è <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: percorsi di esclusione separati da virgola per l'autenticazione del certificato client
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: gli override delle impostazioni dell'applicazione per l'app clonata. Se specificato, queste impostazioni sostituiscono le impostazioni clonate dall'app di origine. In caso contrario, le impostazioni dell'app di origine vengono conservate.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> per clonare nomi host personalizzati dall'app di origine; in caso contrario, <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> per clonare il controllo del codice sorgente dall'app di origine; in caso contrario, <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> per configurare il bilanciamento del carico per l'app di origine e di destinazione.
  - `[CloningInfoCorrelationId <String>]`: ID di correlazione dell'operazione di clonazione. Questo ID consente di creare più operazioni di clonazione per usare lo stesso snapshot.
  - `[CloningInfoHostingEnvironment <String>]`: ambiente del servizio app.
  - `[CloningInfoOverwrite <Boolean?>]`: per <code>true</code> sovrascrivere l'app di destinazione; in caso contrario, <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: posizione dell'app di origine, ad esempio Stati Uniti occidentali o Europa del Nord
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM ID risorsa del profilo di Gestione traffico da usare, se presente. L'ID risorsa di Gestione traffico ha il formato /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: nome del profilo di Gestione traffico da creare. Questa operazione è necessaria solo se il profilo di Gestione traffico non esiste già.
  - `[Config <ISiteConfig>]`: configurazione dell'app.
    - `IsPushEnabled <Boolean>`: ottiene o imposta un flag che indica se l'endpoint Push è abilitato.
    - `[ActionMinProcessExecutionTime <String>]`: il tempo minimo necessario per l'esecuzione del processo prima di eseguire l'azione
    - `[ActionType <AutoHealActionType?>]`: azione predefinita da eseguire.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> se l'opzione Sempre attivato è abilitata; in caso contrario. <code>false</code>
    - `[ApiDefinitionUrl <String>]`: URL della definizione dell'API.
    - `[ApiManagementConfigId <String>]`: APIM-Api identificatore.
    - `[AppCommandLine <String>]`: riga di comando dell'app da avviare.
    - `[AppSetting <INameValuePair[]>]`: impostazioni dell'applicazione.
      - `[Name <String>]`: per associare il nome.
      - `[Value <String>]`: per associare il valore.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> se è abilitata l'opzione Correzione automatica; in caso contrario, <code>false</code> .
    - `[AutoSwapSlotName <String>]`: consente di scambiare automaticamente il nome dello slot.
    - `[ConnectionString <IConnStringInfo[]>]`: stringhe di connessione.
      - `[ConnectionString <String>]`: valore della stringa di connessione.
      - `[Name <String>]`: nome della stringa di connessione.
      - `[Type <ConnectionStringType?>]`: tipo di database.
    - `[CorAllowedOrigin <String[]>]`: ottiene o imposta l'elenco di origini che dovrebbe essere consentito per effettuare chiamate tra origini (ad esempio: http://example.com:12345) . Usare "*" per consentire tutto.
    - `[CorSupportCredentials <Boolean?>]`: ottiene o imposta se le richieste CORS con credenziali sono consentite. Per         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         altre informazioni, vedere.
    - `[CustomActionExe <String>]`: eseguibile da eseguire.
    - `[CustomActionParameter <String>]`: parametri per l'eseguibile.
    - `[DefaultDocument <String[]>]`: documenti predefiniti.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione degli errori dettagliata; in caso contrario, <code>false</code> .
    - `[DocumentRoot <String>]`: radice del documento.
    - `[DynamicTagsJson <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag dinamici che verranno valutati dalle attestazioni degli utenti nell'endpoint di registrazione push.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: elenco di regole di configurazione.
      - `[ActionHostName <String>]`: nome host di uno slot a cui verrà reindirizzato il traffico, se deciso. Ad esempio myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: nell'estensione del sito TiPGle è possibile specificare l'URL per l'algoritmo di decisione personalizzato. Vedere l'estensione di sito TiP All'interno del sito per l'ambito e i contratti.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: specifica l'intervallo in minuti per la valutazione di ReroutePercentage.
      - `[ChangeStep <Double?>]`: nello scenario di avvio automatico questo è il passaggio da cui aggiungere/rimuovere fino a <code>ReroutePercentage</code> raggiungere \n <code>MinReroutePercentage</code> o         <code>MaxReroutePercentage</code> . Le metriche del sito vengono controllate ogni N minuti specificati in .\nCustom decision algorithm può essere fornito nell'estensione del sito TiPTip, in cui è possibile <code>ChangeIntervalInMinutes</code> specificare l'URL. <code>ChangeDecisionCallbackUrl</code>
      - `[MaxReroutePercentage <Double?>]`: specifica il limite superiore sotto il quale reroutePercentage rimarrà.
      - `[MinReroutePercentage <Double?>]`: specifica il limite inferiore al di sopra del quale resterà ReroutePercentage.
      - `[Name <String>]`: nome della regola di routing. Il nome consigliato deve puntare all'slot che riceverà il traffico nell'esperimento.
      - `[ReroutePercentage <Double?>]`: percentuale del traffico a cui verrà reindirizzato <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: stato del servizio FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: mapping del gestore.
      - `[Argument <String>]`: gli argomenti della riga di comando da passare al processore script.
      - `[Extension <String>]`: le richieste con questa estensione verranno gestite con l'applicazione FastCGI specificata.
      - `[ScriptProcessor <String>]`: il percorso assoluto dell'applicazione FastCGI.
    - `[HealthCheckPath <String>]`: percorso per la verifica dell'integrità
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: configura un sito Web per consentire ai client di connettersi tramite http2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se è abilitata la registrazione HTTP; in caso contrario, <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: restrizioni di sicurezza IP per principale.
      - `[Action <String>]`: consente o nega l'accesso per l'intervallo IP.
      - `[Description <String>]`: descrizione della regola di restrizione IP.
      - `[IPAddress <String>]`: indirizzo IP per cui la restrizione di sicurezza è valida.         Può essere in forma di indirizzo ipv4 (proprietà SubnetMask obbligatoria) o notazione CIDR, ad esempio ipv4/mask (corrispondenza di bit iniziale). Per ciDR, non è necessario specificare la proprietà SubnetMask.
      - `[Name <String>]`: nome della regola di restrizione IP.
      - `[Priority <Int32?>]`: priorità della regola di restrizione IP.
      - `[SubnetMask <String>]`: maschera di subnet per l'intervallo di indirizzi IP per cui la restrizione è valida.
      - `[SubnetTrafficTag <Int32?>]`: (interno) Tag di traffico subnet
      - `[Tag <IPFilterTag?>]`: definisce per cosa verrà usato questo filtro IP. In questo modo vengono supportati i filtri IP nei proxy.
      - `[VnetSubnetResourceId <String>]`: ID risorsa di rete virtuale
      - `[VnetTrafficTag <Int32?>]`: tag traffico Vnet (interno)
    - `[JavaContainer <String>]`: Java contenitore.
    - `[JavaContainerVersion <String>]`: Java versione del contenitore.
    - `[JavaVersion <String>]`: Java versione.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: utilizzo massimo consentito delle dimensioni del disco in MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: utilizzo massimo della memoria consentito in MB.
    - `[LimitMaxPercentageCpu <Double?>]`: percentuale massima di utilizzo della CPU consentita.
    - `[LinuxFxVersion <String>]`: App Framework e versione Linux
    - `[LoadBalancing <SiteLoadBalancing?>]`: bilanciamento del carico del sito.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> per abilitare MySQL locale; in caso contrario, <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: limite di dimensioni della directory dei log HTTP.
    - `[MachineKeyDecryption <String>]`: algoritmo usato per la decrittografia.
    - `[MachineKeyDecryptionKey <String>]`: chiave di decrittografia.
    - `[MachineKeyValidation <String>]`: convalida MachineKey.
    - `[MachineKeyValidationKey <String>]`: codice di convalida.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: modalità pipeline gestita.
    - `[ManagedServiceIdentityId <Int32?>]`: ID identità servizio gestito
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura la versione minima di TLS necessaria per le richieste SSL
    - `[NetFrameworkVersion <String>]`: .NET Framework versione.
    - `[NodeVersion <String>]`: versione di Node.js.
    - `[NumberOfWorker <Int32?>]`: numero di dipendenti.
    - `[PhpVersion <String>]`: versione di PHP.
    - `[PowerShellVersion <String>]`: versione di PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: numero di istanze preWarmed.         Questa impostazione si applica solo ai piani a consumo ed elastici
    - `[PublishingUsername <String>]`: nome utente di pubblicazione.
    - `[PushKind <String>]`: tipo di risorsa.
    - `[PythonVersion <String>]`: versione di Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se è abilitato il debug remoto; in caso contrario, <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: versione di debug remoto.
    - `[RequestCount <Int32?>]`: numero richieste.
    - `[RequestTimeInterval <String>]`: intervallo di tempo.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> se la traccia della richiesta è abilitata, in caso contrario <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: consente di richiedere la scadenza della traccia.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: restrizioni di sicurezza IP per scm.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: restrizioni di sicurezza IP per l'uso principale di scm.
    - `[ScmType <ScmType?>]`: tipo SCM.
    - `[SlowRequestCount <Int32?>]`: numero richieste.
    - `[SlowRequestTimeInterval <String>]`: intervallo di tempo.
    - `[SlowRequestTimeTaken <String>]`: tempo impiegato.
    - `[TagWhitelistJson <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag che sono elencati per l'uso dall'endpoint di registrazione push.
    - `[TagsRequiringAuth <String>]`: ottiene o imposta una stringa JSON contenente un elenco di tag che richiedono l'autenticazione dell'utente da usare nell'endpoint di registrazione push.         I tag possono essere costituiti da caratteri alfanumerici e i seguenti: '_', '@', '#', '.', ':', '-'.         La convalida deve essere eseguita in PushRequestHandler.
    - `[TracingOption <String>]`: per le opzioni di traccia.
    - `[TriggerPrivateBytesInKb <Int32?>]`: una regola basata su byte privati.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: una regola basata sui codici di stato.
      - `[Count <Int32?>]`: numero richieste.
      - `[Status <Int32?>]`: codice di stato HTTP.
      - `[SubStatus <Int32?>]`: consente di richiedere lo stato secondario.
      - `[TimeInterval <String>]`: intervallo di tempo.
      - `[Win32Status <Int32?>]`: codice di errore Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: per usare il processo di lavoro a <code>true</code> 32 bit; in caso contrario, <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: applicazioni virtuali.
      - `[PhysicalPath <String>]`: percorso fisico.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> se è abilitato il precaricamento; in caso contrario, <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: directory virtuali per l'applicazione virtuale.
        - `[PhysicalPath <String>]`: percorso fisico.
        - `[VirtualPath <String>]`: percorso dell'applicazione virtuale.
      - `[VirtualPath <String>]`: percorso virtuale.
    - `[VnetName <String>]`: nome rete virtuale.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket è abilitato; in caso contrario, <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon App Framework and version
    - `[XManagedServiceIdentityId <Int32?>]`: ID identità del servizio gestito esplicito
  - `[ContainerSize <Int32?>]`: dimensioni del contenitore di funzioni.
  - `[DailyMemoryTimeQuota <Int32?>]`: quota massima di tempo di memoria giornaliera consentita (applicabile solo alle app dinamiche).
  - `[Enabled <Boolean?>]`: <code>true</code> se l'app è abilitata; in caso contrario. <code>false</code> Se si imposta questo valore su false, l'app viene disabilitata (l'app viene disconnessa).
  - `[HostNameSslState <IHostNameSslState[]>]`: gli stati SSL del nome host vengono usati per gestire le associazioni SSL per i nomi host dell'app.
    - `[HostType <HostType?>]`: indica se il nome host è uno standard o un nome host di archivio.
    - `[Name <String>]`: nome host.
    - `[SslState <SslState?>]`: tipo SSL.
    - `[Thumbprint <String>]`: impronta digitale del certificato SSL.
    - `[ToUpdate <Boolean?>]`: impostato su <code>true</code> per aggiornare il nome host esistente.
    - `[VirtualIP <String>]`: indirizzo IP virtuale assegnato al nome host se è abilitato SSL basato su IP.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> per disabilitare i nomi host pubblici dell'app; in caso contrario, <code>false</code> .          Se <code>true</code> , l'app è accessibile solo tramite il processo di gestione delle API.
  - `[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente del servizio app.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: configura un sito Web in modo da accettare solo le richieste https. Reindirizzamento dei problemi per le richieste http
  - `[HyperV <Boolean?>]`: sandbox Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: tipo di identità del servizio gestito.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: elenco delle identità assegnate dall'utente associate alla risorsa. I riferimenti alle chiavi del dizionario delle identità utente verranno ARM ID risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[IsXenon <Boolean?>]`: Obsoleta: sandbox Di Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: modalità di ridondanza del sito
  - `[Reserved <Boolean?>]`: <code>true</code> se riservato; in caso contrario, <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> per interrompere il sito di SCM (KUDU) quando l'app viene interrotta; in caso contrario, <code>false</code> . L'impostazione predefinita è <code>false</code> .
  - `[ServerFarmId <String>]`: ID risorsa del piano di servizio app associato, formattato come: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## COLLEGAMENTI CORRELATI

