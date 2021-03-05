---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: b46ab9b8dee108f6d2126c199e5609d92452b95a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007213"
---
# Switch-AzCloudService

## SYNOPSIS
Scambia i VIP tra due servizi cloud (supporto esteso) di bilanciamento del carico.

## SINTASSI

### CloudServiceName (impostazione predefinita)
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloudService
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Scambia i VIP tra due servizi cloud (supporto esteso) di bilanciamento del carico.

## ESEMPI

### Esempio 1: Cambiare servizio cloud usando il nome
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Il comando precedente richiama l'operazione vipswap nel servizio cloud con nome 'BService' ed eseguirà l'operazione quando l'utente conferma l'azione nella richiesta di conferma.
"BService" con il suo servizio cloud scambiabile.

### Esempio 2: Cambiare servizio cloud usando un oggetto servizio cloud
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

Il comando precedente richiama l'operazione vipswap nel servizio cloud con nome 'BService' ed eseguirà l'operazione quando l'utente conferma l'azione nella richiesta di conferma.
"BService" con il suo servizio cloud scambiabile.

## PARAMETERS

### -AsJob
Eseguire il comando come processo

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

### -Async


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

### -CloudService
Per creare, vedere la sezione NOTE per le proprietà CLOUDSERVICE e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.
L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

```yaml
Type: System.String
Parameter Sets: (All)
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

## OUTPUT

### System.Boolean

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


SERVIZIO <CloudService> CLOUD: 
  - `Location <String>`: posizione della risorsa.
  - `[Configuration <String>]`: specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.
  - `[ConfigurationUrl <String>]`: specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB. L'URL del pacchetto del servizio può essere URI della firma di accesso condiviso da qualsiasi account di archiviazione.         Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: descrive un profilo dell'estensione del servizio cloud.
    - `[Extension <IExtension[]>]`: elenco delle estensioni per il servizio cloud.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può aggiornare automaticamente typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.
      - `[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.         La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.         Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.         Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno
      - `[Name <String>]`: nome dell'estensione.
      - `[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: nome dell'autore del gestore estensioni.
      - `[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per l'applicazione dell'estensione. Se non si specifica la proprietà o si specifica "*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.
      - `[Setting <String>]`: impostazioni pubbliche per l'estensione. Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione. Per l'estensione XML, ad esempio RDP, si tratta dell'impostazione XML per l'estensione.
      - `[SourceVaultId <String>]`: ID risorsa
      - `[Type <String>]`: specifica il tipo dell'estensione.
      - `[TypeHandlerVersion <String>]`: specifica la versione dell'estensione. Specifica la versione dell'estensione. Se questo elemento non viene specificato o come valore viene usato un asterisco (*), viene usata la versione più recente dell'estensione. Se il valore viene specificato con un numero di versione principale e un asterisco come numero di versione secondaria (X.), viene selezionata l'ultima versione secondaria della versione principale specificata. Se si specifica un numero di versione principale e un numero di versione secondaria (X.Y), viene selezionata la versione dell'estensione specifica. Se si specifica una versione, viene eseguito un aggiornamento automatico sull'istanza del ruolo.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: profilo di rete per il servizio cloud.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: elenco di configurazioni di bilanciamento del carico per il servizio cloud.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: elenco di indirizzi IP
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.
        - `[PublicIPAddressId <String>]`: ID risorsa
        - `[SubnetId <String>]`: ID risorsa
      - `[Name <String>]`: nome risorsa
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: ID risorsa
  - `[OSProfile <ICloudServiceOSProfile>]`: descrive il profilo del sistema operativo per il servizio cloud.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: specifica il set di certificati da installare nelle istanze del ruolo.
      - `[SourceVaultId <String>]`: ID risorsa
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: elenco dei riferimenti a vault delle chiavi in SourceVault che contengono certificati.
        - `[CertificateUrl <String>]`: URL di un certificato che è stato caricato come segreto nel Vault della chiave.
  - `[PackageUrl <String>]`: specifica un URL che fa riferimento alla posizione del pacchetto del servizio nel servizio BLOB. L'URL del pacchetto del servizio può essere URI della firma di accesso condiviso da qualsiasi account di archiviazione.         Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: descrive il profilo del ruolo per il servizio cloud.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: elenco dei ruoli per il servizio cloud.
      - `[Name <String>]`: nome della risorsa.
      - `[SkuCapacity <Int64?>]`: specifica il numero di istanze di ruoli nel servizio cloud.
      - `[SkuName <String>]`: il nome della SKU. NOTA: se il nuovo SKU non è supportato nell'hardware in cui è attualmente in esecuzione il servizio cloud, è necessario eliminare e ricreare il servizio cloud o tornare alla SKU precedente.
      - `[SkuTier <String>]`: specifica il livello del servizio cloud. I valori possibili sono <br /><br /> **Standard** <br /><br /> **Di base**
  - `[StartCloudService <Boolean?>]`: (Facoltativo) Indica se avviare il servizio cloud immediatamente dopo la sua creazione. Il valore predefinito è `true` .         Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente. Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio. Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.
  - `[Tag <ICloudServiceTags>]`: tag di risorsa.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: modalità di aggiornamento per il servizio cloud. Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio. Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento.         I valori possibili sono <br /><br />**Automatico**<br /><br />**Manuale** <br /><br />**Simultaneo**<br /><br />         Se non viene specificato, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento. Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.

## COLLEGAMENTI CORRELATI

