---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023731"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Sinossi
Avvia la creazione di un piano di migrazione.

## SINTASSI

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** avvia la creazione di un piano di migrazione.
La creazione di un piano di migrazione è asincrona.
Per visualizzare lo stato del piano di migrazione, usare il cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .

## ESEMPI

### Esempio 1: avviare un piano di migrazione
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Questo comando avvia la creazione di un piano di migrazione per il contenitore legacy denominato OneSDKAzureCloud.
Il comando restituisce un messaggio relativo allo stato del piano e per utilizzare il cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** per informazioni aggiornate.

### Esempio 2: avviare il piano di migrazione per tutti i contenitori di volumi
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Questo comando avvia la creazione di un piano di migrazione per tutti i contenitori del volume legacy nel file di configurazione importato.

## PARAMETRI

### -Tutti
Indica che questo cmdlet avvia le stime del tempo di migrazione per tutti i contenitori del volume nel file di configurazione importato.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
Specifica l'ID univoco della configurazione dell'appliance legacy.

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

### -LegacyContainerNames
Specifica una matrice di nomi di contenitori di volumi per cui creare un piano di migrazione.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
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

### Nessuno

## OUTPUT

### Stringa
Questo cmdlet restituisce lo stato del processo del piano di migrazione se è stato avviato correttamente nell'appliance.

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


