---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181559"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Crea un oggetto configurazione per la distribuzione automatica di patch in una macchina virtuale.

## SINTASSI

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzVMSqlServerAutoPatchingConfig** crea un oggetto di configurazione per l'applicazione automatica delle patch in una macchina virtuale.

## ESEMPI

### Esempio 1: Creare un oggetto di configurazione per configurare la distribuzione automatica di patch
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Questo comando crea un oggetto configurazione per la distribuzione delle patch.
Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.
Questa configurazione abilita la distribuzione di patch che usa questi valori.
Il comando archivia il risultato nella $AutoBackupConfig variabile.
È possibile specificare questo elemento di configurazione per altri cmdlet, ad esempio Set-AzVMSqlServerExtension cmdlet.

## PARAMETERS

### -DayOfWeek
Specifica il giorno della settimana in cui installare gli aggiornamenti.
I valori accettabili per questo parametro sono:
- Domenica
- Lunedì
- Martedì
- Mercoledì
- Giovedì
- Venerdì
- Sabato
- Ogni giorno

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
Indica che è abilitata la distribuzione automatica di patch per la macchina virtuale.
Se si abilita la distribuzione automatica di patch, il cmdlet attiva la modalità interattiva di Windows Update.
Se si disabilita la distribuzione automatica di patch, le impostazioni di Windows Update non vengono modificate.

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
Specifica la durata in minuti della finestra di manutenzione.
La distribuzione automatizzata delle patch evita di eseguire un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno di tale finestra.
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
Specifica l'ora del giorno in cui inizia la finestra di manutenzione.
Questa volta definisce l'inizio dell'installazione degli aggiornamenti.

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
Specifica se includere gli aggiornamenti importanti.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


