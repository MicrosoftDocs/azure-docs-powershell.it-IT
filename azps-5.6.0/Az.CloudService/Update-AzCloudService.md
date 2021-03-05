---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007181"
---
# Update-AzCloudService

## SYNOPSIS
Creare o aggiornare un servizio cloud.
Tenere presente che alcune proprietà possono essere impostate solo durante la creazione del servizio cloud.

## SINTASSI

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Creare o aggiornare un servizio cloud.
Tenere presente che alcune proprietà possono essere impostate solo durante la creazione del servizio cloud.

## ESEMPI

### Esempio 1: Aggiungere l'estensione RDP a un servizio cloud esistente
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Il set di comandi precedente aggiunge un'estensione RDP a un servizio cloud già esistente denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.

### Esempio 2: Rimuovere tutte le estensioni dal servizio cloud
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Sopra il set di comandi vengono rimosse tutte le estensioni dal servizio cloud esistente denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.

### Esempio 3: Rimuovere l'estensione RDP dal servizio cloud
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

L'insieme di comandi precedente rimuove l'estensione RDP dal servizio cloud esistente denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.

### Esempio 4: istanze Scale-Out/Scale-In ruoli
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Sopra il set di comandi mostra come eseguire la scalabilità orizzontale e il numero di istanze del ruolo di scalabilità per il servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.

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

### -InputObject
Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
Eseguire il comando in modo asincrono

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

### -Parameter
Descrive il servizio cloud.
Per creare, vedere la sezione NOTE per le proprietà PARAMETER e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : parametro Identity
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: percorso di identità della risorsa
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: nome dell'istanza del ruolo.
  - `[RoleName <String>]`: nome del ruolo.
  - `[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.
  - `[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento. I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.

PARAMETER: <ICloudService> descrive il servizio cloud.
  - `Location <String>`: posizione della risorsa.
  - `[Configuration <String>]`: specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.
  - `[ConfigurationUrl <String>]`: specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB. L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.         Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: descrive un profilo di estensione del servizio cloud.
    - `[Extension <IExtension[]>]`: elenco delle estensioni per il servizio cloud.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può aggiornare automaticamente typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.
      - `[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.         La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.         Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.         Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno
      - `[Name <String>]`: nome dell'estensione.
      - `[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: nome dell'autore del gestore estensioni.
      - `[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per l'applicazione dell'estensione. Se non si specifica la proprietà o si specifica "*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.
      - `[Setting <String>]`: impostazioni pubbliche per l'estensione. Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione. Per l'estensione XML, ad esempio RDP, questa è l'impostazione XML per l'estensione.
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
  - `[StartCloudService <Boolean?>]`: (Facoltativo) Indica se avviare il servizio cloud subito dopo la sua creazione. Il valore predefinito è `true` .         Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente. Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio. Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.
  - `[Tag <ICloudServiceTags>]`: tag di risorsa.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: modalità di aggiornamento per il servizio cloud. Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio. Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento.         I valori possibili sono <br /><br />**Automatico**<br /><br />**Manuale** <br /><br />**Simultaneo**<br /><br />         Se non viene specificato, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento. Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.

## COLLEGAMENTI CORRELATI

