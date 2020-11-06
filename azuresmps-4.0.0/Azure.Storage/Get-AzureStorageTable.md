---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507032"
---
# Get-AzureStorageTable

## Sinossi
Elenca le tabelle di archiviazione.

## SINTASSI

### TableName (impostazione predefinita)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.

## ESEMPI

### Esempio 1: elencare tutte le tabelle di archiviazione di Azure
```
PS C:\>Get-AzureStorageTable
```

Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.

### Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly
```
PS C:\>Get-AzureStorageTable -Name table*
```

Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.

### Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione.
Per crearlo, puoi usare il cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica il nome della tabella.
Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.
In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefisso
Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.
Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


