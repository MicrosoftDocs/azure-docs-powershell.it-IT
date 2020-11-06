---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521256"
---
# Get-AzureRmDataLakeAnalyticsCatalogItem

## Sinossi
Ottiene un elemento o tipi di elementi del catalogo data Lake Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
**Get-AzureRmDataLakeAnalyticsCatalogItem** ottiene un elemento del catalogo di analisi di dati di Azure Data Lake specificato o ottiene elementi del catalogo di un tipo specificato.

## ESEMPI

### Esempio 1: ottenere un database specificato
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Questo comando ottiene il database specificato.

### Esempio 2: ottenere tabelle in un database e uno schema specificati
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

Questo comando consente di ottenere un elenco di tabelle nel database specificato.

## PARAMETRI

### -Account
Specifica il nome dell'account analisi dati lago.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ItemType
Specifica il tipo di elemento catalogo degli elementi che vengono recuperati o elencati.
I valori accettabili per questo parametro sono i seguenti:

- Database
- Schema
- Assembly
- tavolo
- TableValuedFunction
- TableStatistics
- ExternalDataSource
- Visualizzazione
- Procedura
- Segreto
- Credenziali
- Tipi
- TablePartition

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Specifica il percorso multiparte dell'elemento da recuperare oppure l'elemento padre dell'elenco elementi da elencare.
Le parti del percorso devono essere separate da un punto (.).

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### CatalogItem
Elemento del catalogo specificato.

### Elenco<CatalogItem>
Elenco degli elementi del catalogo specificati sotto il relativo contenitore.

## Note

## COLLEGAMENTI CORRELATI

[Test-AzureRmDataLakeAnalyticsCatalogItem](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


