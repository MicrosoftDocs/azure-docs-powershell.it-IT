---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514499"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Sinossi
Crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.

## ESEMPI

### Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
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
Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.

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
Type: SwitchParameter
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
Questa volta definisce gli aggiornamenti che iniziano a essere installati.

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
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### AutoPatchingSettings
Questo cmdlet restituisce l'oggetto contenente le impostazioni per l'aggiornamento automatico.

## Note

## COLLEGAMENTI CORRELATI

[New-AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


