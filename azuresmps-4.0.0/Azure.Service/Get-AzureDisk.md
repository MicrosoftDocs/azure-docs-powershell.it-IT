---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029816"
---
# Get-AzureDisk

## Sinossi
Ottiene informazioni sui dischi nel repository di Azure disk.

## SINTASSI

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureDisk** ottiene le informazioni sui dischi archiviati nel repository di Azure disk per l'abbonamento corrente.
Questo cmdlet restituisce un elenco di informazioni per tutti i dischi nel repository.
Per visualizzare le informazioni relative a un disco specifico, specificare il nome del disco.

## ESEMPI

### Esempio 1: ottenere informazioni su un disco
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Questo comando recupera i dati sulle informazioni sul disco denominato ContosoDataDisk dall'archivio disco.

### Esempio 2: ottenere informazioni su tutti i dischi
```
PS C:\> Get-AzureDisk
```

Questo comando consente di ottenere informazioni su tutti i dischi nel repository del disco.

### Esempio 3: ottenere informazioni su un disco
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Questo comando consente di ottenere dati per tutti i dischi nel repository del disco che non sono attualmente collegati a una macchina virtuale.
Il comando ottiene le informazioni su tutti i dischi e passa ogni oggetto al cmdlet **Where-Object** .
Questo cmdlet elimina qualsiasi disco che non ha un valore di $Null per la proprietà **legatiai** .
Il comando Formatta l'elenco come tabella usando il cmdlet **Format-Table** .

## PARAMETRI

### -Diskname
Specifica il nome del disco nel repository del disco sul quale questo cmdlet ottiene le informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


