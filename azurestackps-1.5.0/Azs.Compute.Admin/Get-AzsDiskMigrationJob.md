---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491158"
---
# Get-AzsDiskMigrationJob

## Sinossi
Restituisce l'elenco dei processi di migrazione del disco gestito.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### Ottieni
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## Descrizione
Restituisce un elenco dei processi di migrazione del disco.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

Ottenere un processo di migrazione del disco gestito specifico.

### --------------------------ESEMPIO 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

Restituisce un elenco dei processi di migrazione del disco gestito nella posizione locale.

## PARAMETRI

### -Posizione
Posizione della risorsa.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome GUID processo di migrazione.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Parametri dello stato del processo di migrazione del disco.

```yaml
Type: String
Parameter Sets: List
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

### Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob

## Note

## COLLEGAMENTI CORRELATI

