---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023867"
---
# New-AzureQuickVM

## Sinossi
Configura e crea una macchina virtuale di Azure.

## SINTASSI

### Windows (impostazione predefinita)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureQuickVM** configura e crea una macchina virtuale di Azure.
Questo cmdlet può distribuire una macchina virtuale in un servizio Azure esistente.
Questo cmdlet può in alternativa creare un servizio Azure che ospita la nuova macchina virtuale.

## ESEMPI

### Esempio 1: creare una macchina virtuale
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Questo comando crea una macchina virtuale che esegue il sistema operativo Windows in un servizio esistente.
Il cmdlet basa la macchina virtuale sull'immagine specificata.
Il comando specifica il parametro *WaitForBoot* .
Di conseguenza, il cmdlet attende che la macchina virtuale venga avviata.

### Esempio 2: creare una macchina virtuale usando i certificati
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

Il primo comando ottiene i certificati da un archivio e li archivia nella variabile $certs.

Il secondo comando crea una macchina virtuale che esegue il sistema operativo Windows in un servizio esistente da un'immagine.
Per impostazione predefinita, il listener HTTPS di WinRM è abilitato nella macchina virtuale.
Il comando specifica il parametro *WaitForBoot* .
Di conseguenza, il cmdlet attende che la macchina virtuale venga avviata.
Il comando carica un certificato WinRM e X509Certificates nel servizio ospitato.

### Esempio 3: creare una macchina virtuale che esegue il sistema operativo Linux
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

Questo comando crea una macchina virtuale che esegue il sistema operativo Linux da un'immagine.
Questo comando crea un servizio per ospitare la nuova macchina virtuale.
Il comando specifica una posizione per il servizio.

### Esempio 4: creare una macchina virtuale e creare un servizio per ospitare la nuova macchina virtuale
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

Il primo comando ottiene i percorsi usando il cmdlet **Get-AzureLocation** e li archivia nella variabile di matrice $locations.

Il secondo comando ottiene le immagini disponibili usando il cmdlet **Get-AzureVMImage** e li archivia nella variabile di matrice $images.

Il comando finale crea una grande macchina virtuale denominata VirtualMachine25.
La macchina virtuale esegue il sistema operativo Windows.
Si basa su una delle immagini in $Images.
Il comando crea un servizio denominato ContosoService03 per la nuova macchina virtuale.
Il servizio si trova in una posizione in $Locations.

### Esempio 5: creare una macchina virtuale con un nome IP riservato
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

Il primo comando ottiene i percorsi e li archivia nella variabile di matrice $Locations.

Il secondo comando consente di ottenere le immagini disponibili e quindi di archiviarle nella variabile di matrice $Images.

Il comando finale crea una macchina virtuale denominata VirtualMachine27 in base a una delle immagini in $Images.
Il comando crea un servizio in una posizione in $Locations.
La macchina virtuale ha un nome IP riservato, memorizzato in precedenza nella variabile $ipName.

## PARAMETRI

### -AdminUsername
Specifica il nome utente dell'account di amministratore creato da questo cmdlet nella macchina virtuale.

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

### -AffinityGroup
Specifica il gruppo affinità per la macchina virtuale.
Specifica questo parametro o il parametro *location* solo se questo cmdlet crea un servizio Azure per la macchina virtuale.

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

### -AvailabilitySetName
Specifica il nome del set di disponibilità in cui questo cmdlet crea la macchina virtuale.

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

### -Certificati
Specifica un elenco di certificati usati da questo cmdlet per creare il servizio.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
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

Se il sistema operativo guest è il sistema operativo Windows, questo cmdlet salva questi dati come file binario denominato%SYSTEMDRIVE%\AzureData\CustomData.bin.

Se il sistema operativo guest è Linux, questo cmdlet passa i dati usando il file ovf-env.xml.
L'installazione copia il file nella directory/var/lib/waagent.
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

### -DisableGuestAgent
Indica che questo cmdlet disabilita l'agente guest per il provisioning dell'infrastruttura come servizio (IaaS).

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

### -DisableWinRMHttps
Indica che questo cmdlet disabilita la gestione remota di Windows in HTTPS.
Per impostazione predefinita, WinRM è abilitato su HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Specifica una matrice di oggetti server DNS che definisce le impostazioni DNS per la nuova distribuzione.
Per creare un oggetto **dnsserver** , usa il cmdlet **New-AzureDns** .

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Indica che questo cmdlet Abilita WinRM tramite HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Specifica la modalità di memorizzazione nella cache ospitante per il disco del sistema operativo.
I valori validi sono: 

- ReadOnly
- ReadWrite

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

### -ImageName
Specifica il nome dell'immagine del disco utilizzata dal cmdlet per creare il disco del sistema operativo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -InstanceSize
Specifica le dimensioni dell'istanza.
I valori validi sono: 

- Dimensioni minime
- Small
- Medio
- Grande
- ExtraLarge
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Indica che questo cmdlet crea una macchina virtuale basata su Linux.

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
Specifica il nome utente dell'account amministrativo di Linux creato da questo cmdlet nella macchina virtuale.

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

### -Posizione
Specifica il Data Center di Azure che ospita la macchina virtuale.
Se specifichi questo parametro, il cmdlet crea un servizio Azure nella posizione specificata.
Specifica questo parametro o il parametro *AffinityGroup* solo se questo cmdlet crea un servizio Azure per la macchina virtuale.

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

### -MediaLocation
Specifica il percorso di archiviazione di Azure in cui questo cmdlet crea i dischi delle macchine virtuali.

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

### -Nome
Specifica il nome della macchina virtuale creata da questo cmdlet.

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

### -NoExportPrivateKey
Indica che questa configurazione non carica la chiave privata.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Indica che questo cmdlet non aggiunge un endpoint di WinRM per la macchina virtuale.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifica la password per l'account amministrativo.

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

### -ReservedIPName
Specifica il nome IP riservato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseDnsFqdn
Specifica il nome di dominio completo per la ricerca di DNS inverso.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifica il nome di un servizio Azure nuovo o esistente a cui questo cmdlet aggiunge la nuova macchina virtuale.

Se specifichi un nuovo servizio, questo cmdlet la crea.
Per creare un nuovo servizio, devi specificare il *percorso* o il parametro *AffinityGroup* .

Se specifichi un servizio esistente, non specificare la *posizione* o *AffinityGroup*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -SubnetNames
Specifica una matrice di nomi di subnet per la macchina virtuale.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Specifica il nome di una rete virtuale per la macchina virtuale.

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

### -WaitForBoot
Indica che questo cmdlet attende che la macchina virtuale raggiunga lo stato ReadyRole.
Se la macchina virtuale raggiunge uno degli Stati seguenti, il cmdlet non riesce: FailedStartingVM, ProvisioningFailed o ProvisioningTimeout.

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

### -Windows
Indica che questo cmdlet crea una macchina virtuale Windows.

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

### -WinRMCertificate
Specifica un certificato associato a un endpoint di WinRM da questo cmdlet.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
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
Parameter Sets: Windows
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

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureDns](./New-AzureDns.md)


