---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491473"
---
# Stop-AzsDiskMigrationJob

## Sinossi
Annullare un processo di migrazione su disco gestito.

## SINTASSI

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## Descrizione
Annullare un processo di migrazione del disco.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

Annullare un processo di migrazione su disco gestito.

## PARAMETRI

### -Posizione
Posizione della risorsa.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome GUID processo di migrazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob

## Note

## COLLEGAMENTI CORRELATI

