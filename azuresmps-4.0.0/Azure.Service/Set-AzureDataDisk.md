---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029528"
---
# Set-AzureDataDisk

## Sinossi
Modifica la memorizzazione nella cache dell'host di un disco di dati esistente in una macchina virtuale di Azure.

## SINTASSI

### NoResize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Ridimensionare
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureDataDisk** modifica gli attributi della cache di un disco di dati esistente in una macchina virtuale di Azure.
Specificare il disco di dati da aggiornare per il numero di unità logica (LUN).

## ESEMPI

### Esempio 1: modificare la memorizzazione nella cache dell'host per un disco di dati
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Questo comando ottiene le macchine virtuali eseguite nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .
Il comando li passa al cmdlet corrente usando l'operatore pipeline.
Questo cmdlet imposta il disco di dati su LUN 2 della macchina virtuale denominato VirtualMachine07 per usare la memorizzazione nella cache dell'host ReadOnly.
Il comando Aggiorna la macchina virtuale per riflettere le modifiche usando il cmdlet **Update-AzureVM** .

### Esempio 2: modificare la memorizzazione nella cache dell'host per tutti i dischi di dati in una macchina virtuale
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Questo comando ottiene un oggetto per la macchina virtuale denominato VirtualMachine07 nel servizio cloud di ContosoService.
Il comando lo passa al cmdlet **Get-AzureDataDisk** , che recupera i dischi di dati per la macchina virtuale.
Il cmdlet corrente imposta quindi la modalità di memorizzazione nella cache host di ogni disco di dati in ReadWrite.
Il comando Aggiorna la macchina virtuale per riflettere le modifiche.

## PARAMETRI

### -Diskname
Specifica il nome della configurazione del disco dati che questo cmdlet modifica.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> La memorizzazione nella cache del disco non è supportata per i dischi 4 TiB e più grandi. Se alla VM sono allegati più dischi, ogni disco di dimensioni inferiori a 4 TiB supporterà la memorizzazione nella cache.
>
> La modifica dell'impostazione della cache di un disco di Azure si disconnette e riattacca il disco di destinazione. Se si tratta del disco del sistema operativo, la VM viene riavviata. Arrestare tutte le applicazioni o i servizi che potrebbero essere interessati da questa interruzione prima di modificare l'impostazione della cache del disco. Non seguire tali raccomandazioni può determinare il danneggiamento dei dati.

Specifica le impostazioni di memorizzazione nella cache del livello host del disco.
I valori validi sono:

- Nessuno
- ReadOnly
- ReadWrite

```yaml
Type: String
Parameter Sets: NoResize
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
Specifica il LUN per l'unità dati nella macchina virtuale.
I valori validi sono: da 0 a 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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

### -ResizedSizeInGB
Specifica le nuove dimensioni, in gigabyte, per il disco dati.
La nuova dimensione deve essere superiore alle dimensioni correnti.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto macchina virtuale associato al disco di dati.
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

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


