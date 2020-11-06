---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491613"
---
# New-AzureStorageTable

## Sinossi
Crea una tabella di archiviazione.

## SINTASSI

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.

## ESEMPI

### Esempio 1: creare una tabella di archiviazione di Azure
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

Questo comando crea una tabella di archiviazione con il nome tableabc.

### Esempio 2: creare più tabelle di archiviazione di Azure
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

Questo comando crea più tabelle.
Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.

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
Specifica un nome per la nuova tabella.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


