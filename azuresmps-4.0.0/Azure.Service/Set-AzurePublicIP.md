---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023913"
---
# Set-AzurePublicIP

## Sinossi
Aggiunge un IP pubblico a una macchina virtuale di Azure.

## SINTASSI

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzurePublicIP** aggiunge un IP pubblico a una macchina virtuale di Azure.
Se si esegue questo cmdlet per una macchina virtuale esistente, aggiornare la macchina virtuale per implementare le modifiche.
Puoi specificare l'etichetta di un nome di dominio per creare una voce DNS corrispondente per l'IP pubblico.

## ESEMPI

### Esempio 1: aggiungere un IP pubblico a una macchina virtuale esistente
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Questo comando ottiene la macchina virtuale denominata FTPInstance nel servizio denominato FTPInAzure usando il cmdlet **Get-AzureVM** .
Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente aggiunge il nome IP pubblico ftpip.
Il comando passa la macchina virtuale al cmdlet **Update-AzureVM** , che implementa le modifiche.

### Esempio 2: aggiungere un IP pubblico a una nuova macchina virtuale
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Questo comando crea un oggetto di configurazione della macchina virtuale usando il cmdlet **New-AzureVMConfig** .
Il comando passa l'oggetto al cmdlet **Add-AzureProvisioningConfig** , che fornisce una configurazione aggiuntiva.
Il cmdlet corrente aggiunge il nome IP pubblico ftpip.
Il comando passa la configurazione al cmdlet **New-AzureVM** , che crea la macchina virtuale.

### Esempio 3: aggiungere un IP pubblico e un'etichetta a una macchina virtuale esistente
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Questo comando ottiene la macchina virtuale denominata FTPInstance nel servizio denominato FTPInAzure usando il cmdlet **Get-AzureVM** .
Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente aggiunge il nome IP pubblico ftpip e l'etichetta ipname.
Il comando Aggiorna la macchina virtuale, che implementa le modifiche.

### Esempio 4: aggiungere un IP pubblico e un'etichetta a una nuova macchina virtuale
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Questo comando crea un oggetto di configurazione della macchina virtuale e quindi passa tale oggetto a **Add-AzureProvisioningConfig** , che fornisce una configurazione aggiuntiva.
Il cmdlet corrente aggiunge il nome IP pubblico ftpip e l'etichetta ipname.
Il comando crea la macchina virtuale.

## PARAMETRI

### -DomainNameLabel
Specifica il nome da usare per una voce DNS corrispondente per l'indirizzo IP pubblico.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Specifica il periodo di timeout inattività TCP in minuti.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
Specifica il nome IP pubblico.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Specifica la macchina virtuale a cui questo cmdlet aggiunge IP pubblico.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. WindowsAzure. Commands. ServiceManagement. Model. IPersistentVM

## Note

## COLLEGAMENTI CORRELATI

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


