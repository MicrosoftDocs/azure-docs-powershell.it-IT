---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387547"
---
# New-AzDataMigrationMongoDbDatabaseSetting

## Sinossi
Crea l'impostazione di database per la migrazione per la migrazione mongoDb

## SINTASSI

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## Descrizione
Il cmdlet New-AzDataMigrationMongoDbDatabaseSetting crea l'oggetto delle impostazioni di migrazione che specifica il comportamento di eliminazione e velocità effettiva.
L'output è una coppia di valori chiave con il nome della raccolta e il valore dell'impostazione, che può essere usata per richiamare l'attività di migrazione.

## ESEMPI

### Esempio 1
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## PARAMETRI

### -Nome
Nome del database

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -TargetRequestUnit
Valore dell'unità di richiesta livello database dedicato. Se non è impostata, tale raccolta usa il database condiviso RU.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Raccolte
Matrice di oggetti setting della raccolta MongoDb restituiti da New-AzureRmDmsMongoDbDatabaseSetting chiamata.

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. DataMigration. Models. MongoDbDatabaseSetting

## Note

## COLLEGAMENTI CORRELATI
