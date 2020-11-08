---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023693"
---
# Add-AzureDataDisk

## Sinossi
Aggiunge un disco di dati a una macchina virtuale.

## SINTASSI

### CreateNew (impostazione predefinita)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Importazione
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureDataDisk** aggiunge un disco di dati nuovo o esistente a un oggetto macchina virtuale di Azure.
Usa il parametro *CreateNew* per creare un nuovo disco dati con le dimensioni e l'etichetta specificate.
Usa il parametro *Import* per allegare un disco esistente dal repository di immagini.
Usa il parametro *ImportFrom* per allegare un disco esistente da un BLOB in un account di archiviazione.
Puoi specificare la modalità cache host del disco dati allegato.

## ESEMPI

### Esempio 1: importare un disco di dati dal repository
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Questo comando ottiene un oggetto macchina virtuale per la macchina virtuale denominata VirtualMachine07 nel servizio cloud di ContosoService usando il cmdlet **Get-AzureVM** .
Il comando lo passa al cmdlet corrente usando l'operatore pipeline.
Questo comando allega un disco di dati esistente dal repository alla macchina virtuale.
Il disco dati ha un LUN pari a 0.
Il comando Aggiorna la macchina virtuale per riflettere le modifiche usando il cmdlet **Update-AzureVM** .

### Esempio 2: aggiungere un nuovo disco di dati
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Questo comando ottiene un oggetto macchina virtuale per la macchina virtuale denominata VirtualMachine08.
Il comando lo passa al cmdlet corrente.
Questo comando allega un nuovo disco di dati denominato MyNewDisk. vhd.
Il cmdlet crea il disco nel contenitore VHD nell'account di archiviazione predefinito dell'abbonamento corrente.
Il comando Aggiorna la macchina virtuale per riflettere le modifiche.

### Esempio 3: aggiungere un disco dati da una posizione specificata
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Questo comando ottiene un oggetto macchina virtuale per la macchina virtuale denominata database.
Il comando lo passa al cmdlet corrente.
Questo comando allega un disco di dati esistente denominato Disk14. vhd dalla posizione specificata.
Il comando Aggiorna la macchina virtuale per riflettere le modifiche.

## PARAMETRI

### -CreateNew
Indica che questo cmdlet crea un disco di dati.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Specifica l'etichetta del disco per un nuovo disco di dati.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diskname
Specifica il nome di un disco di dati nel repository del disco.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Specifica la dimensione del disco logico, in gigabyte, per un nuovo disco di dati.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Specifica le impostazioni di memorizzazione nella cache del livello host del disco.
I valori validi sono: 

- Nessuno 
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

### -Import
Indica che questo cmdlet importa un disco di dati esistente dal repository di immagini.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Indica che questo cmdlet importa un disco di dati esistente da un BLOB in un account di archiviazione.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
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

### -LUN
Specifica il numero di unità logica (LUN) per l'unità dati nella macchina virtuale.
I valori validi sono: da 0 a 15.
Ogni disco di dati deve avere un LUN univoco.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Specifica la posizione del BLOB in un account di archiviazione di Azure in cui questo cmdlet archivia il disco di dati.
Se non si specifica una posizione, il cmdlet archivia il disco dati nel contenitore VHD nell'account di archiviazione predefinito per l'abbonamento corrente.
Se un contenitore VHD non esiste, il cmdlet crea un contenitore VHD.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
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

### -VM
Specifica l'oggetto macchina virtuale a cui questo cmdlet allega un disco di dati.
Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .

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

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


