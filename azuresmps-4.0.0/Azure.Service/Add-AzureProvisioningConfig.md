---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029844"
---
# Add-AzureProvisioningConfig

## Sinossi
Aggiunge la configurazione di provisioning per una macchina virtuale di Azure.

## SINTASSI

### Windows (impostazione predefinita)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureProvisioningConfig** aggiunge le informazioni di configurazione di provisioning a una configurazione di una macchina virtuale Azure.
Puoi usare l'oggetto Configuration per creare una macchina virtuale.

Questo cmdlet supporta diverse configurazioni di provisioning, inclusi i server Windows autonomi, i server Windows collegati a un dominio Active Directory e i server basati su Linux.

Per creare un server di dominio Active Directory, specificare il nome di dominio completo del dominio Active Directory e le credenziali del dominio di un utente che disponga delle autorizzazioni necessarie per accedere alla macchina virtuale al dominio.

## ESEMPI

### Esempio 1: creare una macchina virtuale autonoma
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Questo comando crea un oggetto di configurazione della macchina virtuale usando il cmdlet **New-AzureVMConfig** .
Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale che esegue il sistema operativo Windows.
La configurazione include il nome utente e la password di amministratore.
Il comando passa la configurazione al cmdlet **New-AzureVM** , che crea la macchina virtuale.

### Esempio 2: creare una macchina virtuale collegata a un dominio
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.
Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale da unire al dominio contoso.
Il comando include il nome utente e la password necessari per accedere alla macchina virtuale al dominio.
La configurazione richiede all'utente di cambiare la password dell'utente al primo accesso.
Il comando crea la macchina virtuale in base all'oggetto provisioning.

### Esempio 3: creare una macchina virtuale basata su Linux
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.
Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale che esegue il sistema operativo Linux.
La configurazione include il nome utente e la password radice.
Il comando crea la macchina virtuale in base all'oggetto provisioning.

### Esempio 4: creare una macchina virtuale che include i certificati per WinRM
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Il primo comando ottiene i certificati da un archivio certificati e li archivia nella variabile di matrice $certs.

Il secondo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.
Il cmdlet corrente aggiunge la configurazione di provisioning che include i certificati per WinRM.
Il comando crea la macchina virtuale in base all'oggetto provisioning.

### Esempio 5: creare una macchina virtuale con WinRM abilitato tramite HTTP
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.
Il cmdlet corrente aggiunge la configurazione di provisioning con WinRM abilitato tramite HTTP.
Il comando crea la macchina virtuale in base all'oggetto provisioning.

### Esempio 6: creare una macchina virtuale con WinRM disabilitato tramite HTTPS
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.
Il cmdlet corrente aggiunge la configurazione di provisioning che disattiva WinRM tramite HTTPS.
Il comando crea la macchina virtuale in base all'oggetto provisioning.

### Esempio 7: creare una macchina virtuale senza esportare i tasti
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Il primo comando ottiene i certificati da un archivio certificati e li archivia nella variabile di matrice $certs.

Il secondo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.
Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale che include i certificati e non Esporta le chiavi private.
Il comando crea la macchina virtuale in base all'oggetto provisioning.

## PARAMETRI

### -AdminUsername
Specifica il nome utente dell'account di amministratore creato dalla configurazione nella macchina virtuale.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificati
Specifica un set di certificati installati dalla configurazione nella macchina virtuale.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
Specifica un file di dati per la macchina virtuale.
Questo cmdlet codifica il contenuto del file come Base64.
Il file deve essere di lunghezza inferiore a 64 kilobyte.

Se il sistema operativo guest è il sistema operativo Windows, questa configurazione salva questi dati come file binario denominato%SYSTEMDRIVE%\AzureData\CustomData.bin.

Se il sistema operativo guest è Linux, questa configurazione passa i dati usando il file ovf-env.xml.
La configurazione copia il file nella directory/var/lib/waagent.
L'agente archivia anche i dati codificati base64 in/var/lib/waagent/CustomData.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutomaticUpdates
Indica che questa configurazione Disabilita gli aggiornamenti automatici.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Indica che questa configurazione Disabilita l'agente guest dell'infrastruttura come servizio (IaaS).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSSH
Indica che questa configurazione Disabilita SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Indica che questa configurazione Disabilita Windows Remote Management (WinRM) in HTTPS.
Per impostazione predefinita, WinRM è abilitato su HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain
Specifica il nome del dominio dell'account con l'autorizzazione per aggiungere il computer a un dominio.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Specifica la password dell'account utente con l'autorizzazione per aggiungere il computer a un dominio.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Specifica il nome dell'account utente che dispone delle autorizzazioni per aggiungere il computer a un dominio.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Indica che questa configurazione Abilita WinRM su HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain
Specifica il nome di dominio completo (FQDN) del dominio a cui partecipare.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Indica che questa configurazione crea una configurazione Linux.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Specifica il nome utente dell'account amministrativo di Linux creato dalla configurazione nella macchina virtuale.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineObjectOU
Specifica il nome completo dell'unità organizzativa in cui la configurazione crea l'account del computer.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Indica che questa configurazione non carica la chiave privata.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Indica che questa configurazione crea una macchina virtuale senza un endpoint desktop remoto.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Indica che questa configurazione crea una macchina virtuale senza un endpoint SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Indica che questa configurazione crea una macchina virtuale senza una password SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Indica che questa configurazione non aggiunge un endpoint di WinRM per la macchina virtuale.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifica la password dell'account di amministratore.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResetPasswordOnFirstLogon
Indica che la macchina virtuale richiede all'utente di cambiare la password al primo accesso.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Specifica le coppie di chiavi SSH.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Specifica le chiavi pubbliche di SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeZone
Specifica il fuso orario per la macchina virtuale, ad esempio ora solare Pacifico o ora solare fuso centrale Canada.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Specifica un oggetto macchina virtuale.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Indica che questa configurazione crea una macchina virtuale autonoma che esegue il sistema operativo Windows.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsDomain
Indica che questa configurazione crea Windows Server aggiunto a un dominio Active Directory.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Specifica un certificato che questa configurazione associa a un endpoint di WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Specifica una matrice di certificati X509 distribuiti in un servizio ospitato.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)


