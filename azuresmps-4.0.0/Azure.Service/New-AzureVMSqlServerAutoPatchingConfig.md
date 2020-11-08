---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029653"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Sinossi
Crea un oggetto Configuration per l'aggiornamento automatico della macchina virtuale.

## SINTASSI

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico della macchina virtuale.

## ESEMPI

### Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

Questo comando crea un oggetto Configuration che può essere usato per configurare l'aggiornamento automatico tramite set-AzureVMSqlServerExtension.

## PARAMETRI

### -DayOfWeek
Specifica il giorno della settimana in cui devono essere installati gli aggiornamenti.

I valori accettabili per questo parametro sono i seguenti:

- Domenica
- Lunedì
- Martedì
- Mercoledì
- Giovedì
- Venerdì
- Sabato
- Quotidiani

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

### -Enable
Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.
Se si Abilita l'applicazione di patch automatica, il cmdlet verrà inserito in modalità interattiva in Windows Update.
Se si disattiva la correzione automatica, le impostazioni di Windows Update non verranno modificate.

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

### -MaintenanceWindowDuration
Specifica la durata della finestra di manutenzione.
La patching automatizzato eviterà l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.
Sono consentiti solo 30 minuti di incrementi.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
Specifica l'ora del giorno in cui viene avviata la finestra di manutenzione.
Questa volta definisce quando si avvia l'installazione degli aggiornamenti e viene arrotondato all'ora.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Specifica se gli aggiornamenti importanti devono essere inclusi.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### AutoPatchingSettings
Questo cmdlet restituisce l'oggetto contenente le impostazioni per l'aggiornamento automatico.

## Note

## COLLEGAMENTI CORRELATI

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


