---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030860"
---
# New-WAPackVM

## Sinossi
Crea una macchina virtuale.

## SINTASSI

### CreateVMFromTemplate (impostazione predefinita)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questi argomenti sono deprecati e verranno rimossi in futuro.
Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.
Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **New-WAPackVM** crea una macchina virtuale.

## ESEMPI

### Esempio 1: creare una macchina virtuale per il sistema operativo Windows usando un modello
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

Il primo comando crea un oggetto **PSCredential** e lo archivia nella variabile $Credentials.
Il cmdlet richiede l'accesso a un account e una password.
Per altre informazioni, digitare `Get-Help Get-Credential` .

Il secondo comando ottiene il modello di macchina virtuale denominato ContosoTemplate04 usando il cmdlet **Get-WAPackVMTemplate** e lo archivia nella variabile $template.

Il comando finale crea una macchina virtuale denominata ContosoV023, in base al modello archiviato nella variabile $Template.
Il comando specifica il parametro *Windows* e, di conseguenza, la macchina virtuale deve eseguire una versione del sistema operativo Windows.

### Esempio 2: creare una macchina virtuale per il sistema operativo Linux usando un modello
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

Il primo comando crea un oggetto **PSCredential** e lo archivia nella variabile $Credentials.

Il secondo comando ottiene il modello di macchina virtuale denominato ContosoTemplate19 usando il cmdlet **Get-WAPackVMTemplate** e lo archivia nella variabile $template.

Il comando finale crea una macchina virtuale denominata ContosoV028, in base al modello archiviato nella variabile $Template.
Il comando specifica il parametro *Linux* e, di conseguenza, la macchina virtuale deve eseguire una versione del sistema operativo Linux.

### Esempio 3: creare una macchina virtuale da un profilo disco e dimensioni del sistema operativo
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

Il primo comando ottiene un disco del sistema operativo denominato ContosoDiskOS usando il cmdlet **Get-WAPackVMOSDisk** e lo archivia nella variabile $OSDisk.

Il secondo comando ottiene il profilo di dimensione denominato MediumSizeVM usando il cmdlet **Get-WAPackVMSizeProfile** e lo archivia nella variabile $SizeProfile.

Il comando finale crea una macchina virtuale denominata ContosoV073 dal disco del sistema operativo archiviato in $OSDisk e il profilo delle dimensioni archiviato in $SizeProfile.

## PARAMETRI

### -AdministratorSSHKey
Specifica la chiave Secure Shell (SSH) per l'account Administrator.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Indica che il cmdlet crea una macchina virtuale per l'esecuzione del sistema operativo Linux.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica un nome per la macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSDisk
Specifica un disco del sistema operativo come oggetto **VirtualHardDisk** .
Per ottenere un disco del sistema operativo, usare il cmdlet **Get-WAPackVMOSDisk** .

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Specifica un codice Product Key.
Il codice Product Key è un numero di 25 cifre che identifica la licenza del prodotto.
Usare un codice Product Key per un sistema operativo che si prevede di installare in una macchina virtuale o in un host.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Modello
Specifica un modello.
Il cmdlet crea una macchina virtuale in base al modello specificato.
Per ottenere un oggetto modello, usare il cmdlet Get-WAPackVMTemplate.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Specifica le credenziali per l'account di amministratore locale.
Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .
Per altre informazioni, digitare `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Specifica un profilo di dimensione per una macchina virtuale come oggetto **HardwareProfile** .
Per ottenere un profilo di dimensione, usare il cmdlet **Get-WAPackVMSizeProfile** .

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Specifica una rete virtuale.
Il cmdlet connette la macchina virtuale alla rete virtuale specificata.
Per ottenere una rete virtuale, usare il cmdlet **Get-WAPackVNet** .

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Indica che il cmdlet crea una macchina virtuale per l'esecuzione del sistema operativo Windows.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Riavviare-WAPackVM](./Restart-WAPackVM.md)

[Curriculum vitae-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Start-WAPackVM](./Start-WAPackVM.md)

[Stop-WAPackVM](./Stop-WAPackVM.md)

[Suspend-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


