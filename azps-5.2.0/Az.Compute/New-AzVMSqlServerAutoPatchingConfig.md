---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331891"
---
# New-AzVMSqlServerAutoPatchingConfig

## Sinossi
Crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.

## SINTASSI

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.

## ESEMPI

### Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Questo comando crea l'oggetto Configuration per la creazione di patch.
Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.
Questa configurazione consente di applicare le patch che usano questi valori.
Il comando Archivia il risultato nella variabile $AutoBackupConfig.
Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzVMSqlServerExtension.

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
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.
Se si Abilita la patching automatizzato, il cmdlet inserisce Windows Update in modalità interattiva.
Se si disattiva l'aggiornamento automatico, le impostazioni di Windows Update non cambiano.

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

### -MaintenanceWindowDuration
Specifica la durata, in minuti, della finestra di manutenzione.
La correzione automatica consente di evitare l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.
Specificare un multiplo di 30 minuti.

```yaml
Type: System.Int32
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
Questa volta definisce gli aggiornamenti che iniziano a essere installati.

```yaml
Type: System.Int32
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
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Compute. AutoPatchingSettings

## Note

## COLLEGAMENTI CORRELATI

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


